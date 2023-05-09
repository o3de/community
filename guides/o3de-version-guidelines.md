# O3DE Version Guide

> **Process Owner**: sig-core

Related RFC: [Engine, Project and Gem Versions](https://github.com/o3de/sig-core/issues/44)

For more information about how versioning is used in O3DE see the [Engine Versioning](https://www.o3de.org/docs/contributing/release-versioning-and-terms/) and [Gem Versioning](https://www.o3de.org/docs/user-guide/gems/gem-versioning/) documentation.

## O3DE Version Numbering 
O3DE uses `MAJOR.MINOR.PATCH` [semantic versioning](https://semver.org/)  for all the version fields in `engine.json`, `gem.json` and `project.json` files.

- `MAJOR` is for API-breaking changes
- `MINOR` is for non-API-breaking changes that add new APIs or change them in a non-breaking way
- `PATCH` is for all other non-API-breaking changes, usually important fixes

Example: If a breaking API change is made to a gem at version `2.0.1` the `MAJOR` version is incremented and the `MINOR` and `PATCH` are reset to 0 resulting in the new version being `3.0.0`. See the [semantic versioning](https://semver.org/) page for more examples.

## O3DE Version Specifiers 

Lists of compatible engines and dependencies use the `<name><version specifier>` format based on [PEP 440](https://peps.python.org/pep-0440/#version-specifiers).

Examples:

| Name | Version Specifier | Combined | Description |
|------|-------------------|----------|-------------|
| o3de | >=2.0.0           | o3de>=2.0.0 | o3de version 2.0.0 or greater |
| o3de-sdk | == 1.2.0      | o3de-sdk==1.2.0 |  o3de-sdk version 1.2.0 | 
| Atom | ~=2.0.0           | Atom~=2.0.0 | Atom version 2.0.0 up to but not including 3.0.0 |

A gem that is known to be compatible with the an engine named `o3de-sdk` version `2.0.1` could include `o3de-sdk==2.0.1` in the `compatible_engines` field in `gem.json`

## Guidelines for the `engine.json` '`version`' field 

### API changes

When you make a change to a `version` field in a `gem.json` file or `engine.json` `api_versions` entry, you should make the same change to the `version` field in `engine.json`.  This provides an overall indication that some important API change has been made in O3DE.  Ideally, this process will be automated, but is not critical.

Example:

A developer increments the `MINOR` version of the `Atom` `gem.json` and resets the `PATCH` version, the developer also should increment the `MINOR` version and reset the `PATCH` version to zero for the `version` field in `engine.json`

Changes: 
1. `gem.json` version `2.3.1` -> `2.4.0`
2. `engine.json` version `15.3.2` -> `15.4.0` 

### Stabilization processes

When a new `stabilization/XXYY` branch is created the following changes should be made:
1. Increment the `MINOR` version and reset the `PATCH` version to '0' in `engine.json` in the new `stabilization/XXYY` branch.
2. Increment the `MAJOR` version and reset the `MINOR` and `PATCH` versions to '0' in `engine.json` in the `development branch.

These changes are made to prevent O3DE from having two branches with the same version.

