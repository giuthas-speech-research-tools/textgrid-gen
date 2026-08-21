# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

[//]: # (Possible headings in a release:)
[//]: # (Highlights for shiny new features.)
[//]: # (Added for new features.)
[//]: # (Changed for changes in existing functionality.)
[//]: # (Refactor when functionality does not change but moves.)
[//]: # (Documentation for updates to docs.)
[//]: # (Testing for updates to tests.)
[//]: # (Deprecated for soon-to-be removed features.)
[//]: # (Removed for now removed features.)
[//]: # (Fixed for any bug fixes.)
[//]: # (Security in case of vulnerabilities.)
[//]: # (New contributors for first contributions.)

[//]: # (And ofcourse if a version needs to be YANKED:)
[//]: # (## [version number] [data] [YANKED])


## [Unreleased]

### Added

- `tggen` will be available from version 0.3.0 or soon after on pypi.
- 0.4.0 will add two commands as detailed below.
- 1.0 will do some code clean up
- 1.x will potentially add new commands and new configuration options. Send me
  an email or open on issue to request some?


## [0.4.0] 2026-??-?? Unreleased

### Highlights

- This version will add commands `init` and `add`.

### Added

- `init` initialises the directory structure used by `tggen`. 
- `add` applies exclusion list before processing files.
- `add` moves existing textgrids to a safe directory before creating new tiers
  and writing the new textgrids in the original directory.
- `add` now does incremental adding of Tiers.
- Documentation for the directory structure and the commands in
  docs/Directories.
- A number of other commands are present in the command line interface too, but
  have not been implemented yet.


## [0.3.0] 2026-08-

### Highlights

- test-pypi and pypi uploads
- New installation procedure with `uv`.

### Added

- Some new documentation.

### Removed

- Removed all conda and mamba related files.
- File tier level is now by default off even if it is not explicitly set in the
  configuration.
- Similarly, Utterance, Word, Phoneme, and Phone are by default on.
- Removed read_na_list which was used to read old style exclusion text files.


## [0.2.0] 2025-03-26

### Highlights

- `align-beeps` and `split-tier` added.

### Added

- `align-beeps` automatically aligns manually or otherwise placed boundaries on
  a named Tier to beeps.
- `split-tier` splits the named Tier in a TextGrid into two by moving every
  other boundary to one new Tier and every other to the other.

### Fixed

- Bugs in beep detection. 


## [0.1.0] 2024-10-08

### Added

- After installation CAST can now be executed as a regular command -- `cast` or
  `computer_assisted_segmentation_tools` from the commandline (no need to call
  Python or run it from a specific directory).
- `cast add` now works for utterance Tiers for TextGrids newly generated from AAA
  metadata. 

### Removed

- Old commandline script at project root.
- Support for yaml config files that had spaces in variable names.

### Known issues

- `concatenate` does not work yet, nor does `add` yet work with concatenated
  data.
