# O3DE Deprecation Guide

> **Process Owner**: sig-release
>
> **Note**: This is a living document and is subject to change. Please contact [sig-release](https://github.com/o3de/sig-release) via [GitHub](https://github.com/o3de/sig-release/issues) or [Discord](https://discord.gg/crRVGNh9vu) to discuss any updates or amendments to the document.
>
> *How to request changes*
>
> - For a small change (e.g. spelling/grammar/formatting), please create a [GitHub issue](https://github.com/o3de/sig-content/issues/new/choose) or [pull request](https://github.com/o3de/sig-content/pulls) against the [Community repo](https://github.com/o3de/community) with the fix).
> - For a large change (e.g. changes to process), please create an [RFC](https://github.com/o3de/sig-release/issues/new/choose) for sig-release with the proposed change and reasons why (see [RFC suggestion request template](https://github.com/o3de/sig-release/issues/new?assignees=&labels=rfc-suggestion&template=rfc-suggestion.md&title=Proposed+RFC+Suggestion+%3Ddescription%3D) for more details).

## Deprecation Types

- API Deprecation
- Feature/System Deprecation

## API Deprecation

An overview of how to make breaking API changes/removals

### API Deprecation - Examples

- Renaming a function
- Renaming a class/EBus
- Changing a function signature
- Removing a function

### API Deprecation - Initial Steps

- Identify the code to be deprecated (something resembling one of the API deprecation examples above)
  - Create a new GitHub issue with the name *"Deprecate \<Function/Type Name\>"*
    - Add the `"kind/deprecation"` label
    - In the description, add a preliminary release note (what do you want to say to the customer about this change)
      - (if available) Add a milestone label for which release this deprecation will be part of
  - In the code, add an `O3DE_DEPRECATION_NOTICE(<GHI Number>)` comment right above the API call

    ```c++
    // e.g.
    // O3DE_DEPRECATION_NOTICE(GHI-1234)
    AZ::Entity* CreateEditorEntity(const char* name) = 0;
    ```

    - Add an announcement to the Discord Impactful Change channel
      - Note: If you do not have permissions for this, please contact the sig your deprecation applies to and someone will post the impactful change announcement on your behalf

### Tracking

- sig-release can filter GHIs by date and label (e.g. `"kind/deprecation"`) to author Release Notes

### Advice

- Use of the `AZ_DEPRECATED` macro is not allowed when first deprecating an API
  - It is required to first use the comment identifier `O3DE_DEPRECATION_NOTICE`, and as a second pass, add `AZ_DEPRECATED`
  - Note: In C++ code, `@deprecated` may be used to highlight deprecation changes in the API reference. This is not widely supported and is not a requirement at this time

## System/Feature Deprecation

An overview of how to make breaking System/Feature changes/removals

### System/Feature Deprecation Examples

- Removing a Gem
- Removing an Editor feature
- Removing a library

### System/Feature Deprecation - Initial Steps

- Create an RFC in the appropriate sig (e.g. [sig-content](https://github.com/o3de/sig-content), [sig-simulation](https://github.com/o3de/sig-simulation)) to notify the community of the system to be deprecated
  - Include why it's being removed and identify alternatives if customers depend on 'X' feature
    - As part of the RFC determine a deprecation schedule
    - Add who (e.g. sig responsible) to contact
    - Add an announcement to the Discord Impactful Change or relevant sig channel (when publishing the RFC and when it is either approved or rejected)
      - Note: If you do not have permissions for this, please contact the sig your deprecation applies to and someone will post the impactful change announcement on your behalf
      - Include an announcement at initial proposal time and at the time of removal
    - Deprecations should form part of the release notes and be highlighted in a features documentation
      - To support this, please create a GitHub issue with title *"Deprecate \<Feature/System Name\>"*
      - Add the `"kind/deprecation"` label
      - In the description, add a preliminary release note (what do you want to say to the customer about this change)
      - (if available) Add a milestone label for which release this deprecation will be part of

## Philosophy

- When modifying existing code that external customers rely on, we should strive wherever possible to not break them when making changes
- If code is to be changed or removed, we should let customers know ahead of time with a reasonable notice period (approximately 1 release (2-3 months))

## Migrations/Backwards Compatibility

- For changes to underlying data formats, it is the developers responsibility (where possible) to provide a migration/upgrade process to allow customers to move to the new format with as little overhead as possible (e.g. Version converters used with the Serialize Context and Object Stream in C++).
- Note: This advice applies for changes as opposed to total removals. If it is not practical or possible to provide an automated conversion, guidance/steps should be documented to help users adjust to the change manually.
- *Note: Additional information on data migrations is lacking and will be added in future.*

## Stable vs Volatile APIs

- For new code with few users depending on it, much weaker guarantees can be made about breaking changes.
- The source of truth for this is the [sig feature matrix](https://github.com/o3de/community/tree/main/features/sigjson) for a given feature. If a new feature is under active development and no promises have yet been made about API stability, the deprecation policy does not apply. If however an API is mature and widely used, an unannounced breaking change is not acceptable. The policy of first documenting/announcing a deprecation, and then following-up with a change in future to give customers time to upgrade is required
- Note: For improved visibility, owners of the sig feature matrix should include file paths in the notes section that are explicitly excluded from the deprecation policy if the API is volatile
