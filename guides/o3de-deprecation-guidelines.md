# O3DE Deprecation Guide

> **Process Owner**: sig-release
>
> **Note**: This is a living document and is subject to change. Please contact [sig-release](https://github.com/o3de/sig-release) via [GitHub](https://github.com/o3de/sig-release/issues) or [Discord](https://discord.gg/crRVGNh9vu) to discuss any updates or amendments to the document.
>
> *How to request changes to this document*
>
> - For a small change (e.g. spelling/grammar/formatting), please create a [GitHub issue](https://github.com/o3de/sig-content/issues/new/choose) or [pull request](https://github.com/o3de/sig-content/pulls) against the [Community repo](https://github.com/o3de/community) with the fix).
> - For a large change (e.g. changes to process), please create an [RFC](https://github.com/o3de/sig-release/issues/new/choose) for sig-release with the proposed change and reasons why (see [RFC suggestion request template](https://github.com/o3de/sig-release/issues/new?assignees=&labels=rfc-suggestion&template=rfc-suggestion.md&title=Proposed+RFC+Suggestion+%3Ddescription%3D) for more details).

## Deprecation Types

- API Deprecation
- Feature/System Deprecation

> **Note:** *All breaking changes are deprecation changes*.

## API Deprecation

An overview of how to make breaking API changes/removals.

In the ideal case, API deprecation would happen over 2 O3DE releases which typically happen every 6 months.
1. In the first release an `O3DE_DEPRECATION_NOTICE` is added, so developers know API  code is being deprecated, but it doesn't cause the compile warnings/errors that `AZ_DEPRECATED` does.
2. In the second release `version` fields are updated and `AZ_DEPRECATED` macros are added, causing code compile warnings for all developers using the methods that can be ignored with compiler flags.
3. After the second release, the code is removed and won't exist in the third release.

In real life it's often not practical for developers to babysit deprecated code over a year or longer.  At minimum, developers should: 
1. Add the `O3DE_DEPRECATION_NOTICE` code comment (see below), so the change can be easily found and added to release notes.
1. Increment the `MAJOR` and zero out the remaining elements in the `version` field in the `gem.json` if inside a gem or `engine.json` if  inside the engine's `Code` folder.  

Developers rely on the `version` field to catch `MAJOR` compatibility changes that make their code no longer compile.  For more information about how versioning is used in O3DE see the [Engine Versioning](https://www.o3de.org/docs/contributing/release-versioning-and-terms/) and [Gem Versioning](https://www.o3de.org/docs/user-guide/gems/gem-versioning/) documentation.

Related RFC: [Engine, Project and Gem Versions](https://github.com/o3de/sig-core/issues/44)

### API Deprecation - Examples

- Renaming a function
- Renaming a class/EBus
- Changing a function signature
- Removing a function

### API Deprecation - Initial Steps

1. Identify the code to be deprecated (something resembling one of the API deprecation examples above).

    - Create a new GitHub issue with the name *"Deprecate \<Function/Type Name\>"*, using the [Deprecation Notice](https://github.com/o3de/o3de/issues/new/choose) issue type.
    - Add the `"kind/deprecation"` label.
    - Add the relevant SIG label(s) for code owners ie `SIG/content`
    - In the description, add a preliminary release note (what do you want to say to the customer about this change).
      - (If available) Add a milestone label for which release this deprecation will be part of.
    - Ideally, notify the SIG(s) of the deprecation issue in their respective Discord chat channels.

2. In the code, add an `O3DE_DEPRECATION_NOTICE(<GHI Number>)` comment right above the API call.

    ```c++
    // e.g.
    // O3DE_DEPRECATION_NOTICE(GHI-1234)
    AZ::Entity* CreateEditorEntity(const char* name) = 0;
    ```
    - *Note: If you are replacing an API method with new methods, consider incrementing the MINOR version number in the `gem.json` or engine API you are updating so any developers who depend on the API can reference the new version as the point when the new API methods became available.*

3. Create a pull request referencing the GitHub issue. Code owners will be notified of this change. (Check the [CODEOWNERS](https://github.com/o3de/o3de/blob/development/.github/CODEOWNERS) file to verify which sig the deprecation applies to).

4. Once the PR is approved, add an announcement to the Discord Impactful Change channel and relevant sig channel.

   - *Note: If you do not have permissions for this, please contact the sig your deprecation applies to and someone will post the impactful change announcement on your behalf.*

### Tracking

- [sig-release](https://github.com/o3de/sig-release) can filter GitHub issues by date and label (e.g. `"kind/deprecation"`) to author release notes.

### Advice

- Use of the `AZ_DEPRECATED` macro should not be used when first deprecating an API.
  - It is required to first use the comment identifier `O3DE_DEPRECATION_NOTICE`, and as a second pass, add `AZ_DEPRECATED` (applies to mature APIs - see [Stable vs Volatile APIs](#stable-vs-volatile-apis)).
  - Note: In C++ code, `@deprecated` may be used to highlight deprecation changes in the API reference. This is not widely supported and is not a requirement at this time.

### API Deprecation - Final Steps

After the `O3DE_DEPRECATION_NOTICE` comment has been present in the code for one O3DE release (typically 6 months):
1. Add the `AZ_DEPRECATED` macro to the API methods.
2. Increment the `MAJOR` element and zero out the other elements in the `version` field in the `gem.json` if gem code or `engine.json` if engine code.

After the `AZ_DEPRECATED` macro has been present in the code for one release, remove the code.

## System/Feature Deprecation

An overview of how to make breaking System/Feature changes/removals.

### System/Feature Deprecation Examples

- Removing a Gem
- Removing an Editor feature
- Removing a library

### System/Feature Deprecation - Initial Steps

1. Create an RFC in the appropriate sig (e.g. [sig-content](https://github.com/o3de/sig-content), [sig-simulation](https://github.com/o3de/sig-simulation)) to notify the community of the system to be deprecated. (Check the [CODEOWNERS](https://github.com/o3de/o3de/blob/development/.github/CODEOWNERS) file if you're unsure which sig the deprecation belongs to).

   - Include why it's being removed and identify alternatives if customers depend on 'X' feature.
   - As part of the RFC determine a deprecation schedule.
   - Add who (e.g. the sig responsible) to contact.

   > **Note:** If consensus within a sig cannot be reached, then escalate the discussion to the Technical Steering Committee ([TSC](https://github.com/o3de/tsc)) for review.

2. Add an announcement to the Discord Impactful Change or relevant sig channel (when publishing the RFC and when it is either approved or rejected).

    - Note: If you do not have permissions for this, please contact the sig your deprecation applies to and someone will post the impactful change announcement on your behalf.
    - Include an announcement at initial proposal time and at the time of removal.

3. Create a GitHub issue with the title *"Deprecate \<Feature/System Name\>"*.

     - Doing this will help ensure that the deprecation becomes part of the next set of release notes, and is highlighted in the feature documentation.
     - In the GitHub issue, add the `"kind/deprecation"` label.
     - In the description, add a preliminary release note (what do you want to say to the customer about this change).
     - (If available) Add a milestone label corresponding to the release that this deprecation will be part of.

## Philosophy

- When modifying existing code that external customers rely on, we should strive wherever possible to not break them when making changes.
  - To avoid this, plan to deprecate the existing code/feature and introduce the new code/feature whether its an API, system or data format, at the same time.
- If code is to be changed or removed, we should let customers know ahead of time with a reasonable notice period (currently 1 full release cycle).

## Migrations/Backwards Compatibility

- For changes to underlying data formats, it is the developer's responsibility (where possible) to provide a migration/upgrade process to allow customers to move to the new format with as little overhead as possible (e.g. Version converters used with the Serialize Context and Object Stream in C++).
- Note: This advice applies for changes as opposed to total removals. If it is not practical or possible to provide an automated conversion, guidance/steps should be documented to help users adjust to the change manually.
- *Note: Additional information on data migrations is lacking and will be added in future.*

## Stable vs Volatile APIs

- For new code with few users depending on it, much weaker guarantees can be made about breaking changes.
- The source of truth for this is the [sig feature matrix](https://github.com/o3de/community/tree/main/features/sigjson) for a given feature. If a new feature is under active development and no promises have yet been made about API stability, the deprecation policy does not apply. If however an API is mature and widely used, an unannounced breaking change is not acceptable. The policy of first documenting/announcing a deprecation, and then following-up with a change in future to give customers time to upgrade is required.
- Note: For improved visibility, owners of the sig feature matrix should include file paths in the notes section that are explicitly excluded from the deprecation policy if the API is volatile.
