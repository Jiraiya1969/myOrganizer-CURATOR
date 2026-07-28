# CURATOR / myOrganizer v1.0.0-beta.2 Changelog

Last updated: July 28, 2026 at 11:23 AM EST

This changelog summarizes new features, improvements, fixes, and known
limitations in each CURATOR release.

## v1.0.0-beta.2 - 2026-07-28

This beta focuses on faster preparation of large collections, safer recovery,
clearer progress reporting, and documentation that is easier to use and keep
with the application.

### Added

- Added this changelog to the application folder so each release clearly
  explains what changed in that specific version.
- Added stronger release-package checks. Future packages must match the
  approved application inventory exactly and must exclude development,
  temporary, and operator-owned files.
- Added the CURATOR-owned Atari 8-Bit and Atari ST routing definitions required
  for a ready-to-use installation. Operator-supplied platform and DAT files
  remain outside the release package.

### Changed

- Large Stage 5 preparation jobs now copy ordinary files and process archives
  in controlled parallel groups. This substantially reduces preparation time
  while keeping results in a predictable order.
- Stage 5 recovery records are written more efficiently, reducing repeated
  bookkeeping during collections containing thousands of files.
- Archive progress is smoother and less noisy. One continuous progress display
  now covers the complete archive workload instead of repeatedly finishing and
  restarting after each recovery checkpoint.
- Matching now passes the exact verified game data forward when a removable
  header or similar supported normalization was needed to establish the match.
- The Admin Guide, End User Manual, Quick Start Guide, and Core API Developer
  Handbook are now supplied as PDF files for easier viewing on systems without
  Microsoft Word.
- The developer handbook now documents all 144 current Core programming
  interfaces. This is primarily useful to contributors and advanced users.

### Fixed

- Fixed Stage 5 archive preparation when the selected Workspace folder is
  outside the CURATOR application folder, which is the normal recommended
  setup.
- Fixed interrupted archive recovery so unfinished archive results are removed
  before that work is retried. Files already committed by CURATOR remain
  protected.
- Fixed empty or unusable archives so they can be reported and skipped without
  ending the entire preparation stage.
- Fixed Stage 5 error reporting so the original problem remains visible even
  if logging services have already closed.
- Fixed matching for supported disc collections when cue-sheet and track
  evidence is needed to confirm the correct result.
- Fixed later stages receiving the original file instead of the verified
  normalized data that established an authoritative match.
- Added a clear, safe cancellation path to both advanced Nuclear cleanup
  confirmations. Only the exact confirmation phrase performs the cleanup.
- Fixed the completion screen shown after generating the Core API handbook.

### Known limitations

- In a pause-enabled multi-stage Gateway run, the final selected stage may not
  show its promised acknowledgement before the separate overall timing
  summary. The stage result and timing summary are still produced.
- If a very large interrupted Stage 5 recovery record is present, Gateway
  startup can take longer while CURATOR validates that saved work. This delay
  occurs before the main menu appears and does not mean the application has
  stopped responding.

## v1.0.0-beta.1 - 2026-07-26

### Added

- Published the first public beta of CURATOR.
- Added guided `Prepare DAR`, `Organize`, and `Reporting` workflows for building
  and reviewing a LaunchBox-compatible collection.
- Added platform and DAT discovery, authority preparation, source-file
  discovery, staging, matching, DAT validation, assembly, completeness
  analysis, physical organization, and collection reporting.
- Added support for authority-based processing of loose files and supported
  archive and disc-image workflows.
- Added recoverable staging and output transactions so interrupted work can be
  resumed from committed progress when recovery evidence remains valid.
- Added `Clear` and `Append` destination choices for controlled output-folder
  handling.
- Added visible progress, structured logs, validation evidence, and final
  collection reports.
- Included an Admin Guide, End User Manual, Quick Start Guide, and Core API
  Developer Handbook.
- Added safeguards that require separate source, output, and working folders
  and prevent normal collection paths from being placed inside the CURATOR
  application folder.

### Known limitations

- In pause-enabled Gateway sequences, the final selected stage may not show its
  promised stage acknowledgement before the separate Gateway timing summary.
  This does not suppress the final timing summary.
