# CURATOR v2.0.0-beta.6 Changelog

Last updated: September 28, 2026

This changelog summarizes new features, improvements, fixes, and known
limitations in each CURATOR release.

## v2.0.0-beta.6 - 2026-09-28

Start a clean run with every BETA release. Saved databases and unfinished runs from an earlier BETA release cannot be reused. Preserve original collections and use copied input.

**MAME support remains very early and experimental. Continue using clrmame to manage MAME collections.**

### Added

- Added newly found disks to their existing ZIP in Incomplete Sets during Append, while preserving existing contents and skipping disks already present. Completed containers remain in Incomplete Sets.

- Added folders for Applications, Educational software, Demos and other recognized catalogue categories within each platform, and Games folders within format-specific folders. Games without a format-specific destination keep their normal platform placement. Existing output is not automatically moved.
- Added Operating System and Revisions folders within each platform's existing folder structure. Operating-system revisions go under Operating System\Revisions. Existing output folders are not automatically moved or renamed.
- Added informational estimates of multi-disk groups, disk sides, parts and companion files. Required members of the selected DAT set determine completeness and output placement; the whole-game limitations are described below.
- Applied language folders where appropriate while keeping USA-inclusive sets at the platform root regardless of language tags.
- Simplified the README and guide warning: antivirus software can interfere with DolphinTool. If DolphinTool reports the error, click **OK** to continue.

### Changed

- Reduced delays when preparing DAT catalogues and checking the saved reference library, while preserving duplicate decisions, original declarations and set memberships.

- Reduced repeated work when preparing incomplete-set archives and final output plans while preserving filenames, contents and set memberships.

- Reduced delays during matching and disc-group checks while preserving match decisions, filenames and set memberships.

- Reduced repeated file checking during matching while preserving results when working files remain unchanged.

- Reduced repeated setup work during collection processing while preserving filenames, file contents and set memberships.

- Reduced delays when preparing large groups of loose files while keeping saved progress available for Resume.

- Organized complete MAME Software List ROM sets under their company’s MAME folder, using software-list and game identifiers while preserving the ROM filenames. MAME Arcade handling remains separate.

- Showed recovery choices in a centered panel on a cleared screen, with readable wrapped text and a details view that stays open until you return.

- Clarified that antivirus and other security software may interrupt processing, with guidance to check security alerts and activity history when access problems occur.

- Showed overall progress and the current file separately while copying, packaging and converting files, with a consistent display while preparing disc images.
- Showed disc-checking messages as they arrive, with a waiting notice during longer checks.
- Used simple messages while clearing the existing collection output.

- Started collection stages through the Gateway, with Clear or Append chosen before processing begins.
- Separated unidentified ordinary files into folders named after their original extensions, such as A26, BIN and JPG, within needs_attention. Files without an extension remain under Unknown File with their contents preserved.
- Showed clearer startup, scanning and output progress, including the current platform, file counts and completed work.
- Placed incomplete sets under one Incomplete Sets folder while keeping their company, media and platform folders.
- Copied files first, then created ZIP packages and converted disc images, with clearer progress for each group.
- Reduced delays when classifying files, planning collection output and starting final file creation, while preserving filenames, contents, set memberships and conflict handling.
- Updated the guides with setup instructions, supported behavior, practical limitations and relevant API contracts. Kept only the latest guides in the documentation folder, with earlier editions available in History.
- Organized the AtariMania ST catalogue into individual disk-image sets, with supporting documents kept separately.
- Simplified review folders by removing the extra Unresolved Media level.
- Named ordinary collection packages after the set name in the selected DAT while preserving the filenames inside each package.
- Removed the need for a separate software-list DTD file during setup.

### Fixed

- Preserved original disc images when copying them for review, and stopping cleanup when a file is outside the working folder or its path contains a directory link.

- Excluded time spent waiting for completion acknowledgments from stage processing times in individual, selected and full runs. Showing overall elapsed time, including waits, separately.

- Showed complete and incomplete DAT-set totals separately from informational whole-game estimates.

- Reduced delays when creating ordinary ZIPs and clearing temporary working files, while preserving completed output and the ability to resume interrupted work.

- Prevented DAT Validation from stopping on correctly matched CHD tracks that also appear in other platforms’ catalogues, while preserving their set memberships.

- Kept the final Stage Summary visible after full runs and Organize until you press Enter, while preserving pauses between stages where selected.

- Showed completed output-planning work against actual totals, including incomplete groups, and showing an activity message when a total is not yet known.

- Showed matching progress against the actual files, reference records and disc groups being processed, and marking result saving complete only after the results are saved.

- Reused the original working folders when resuming interrupted archive preparation, avoiding redundant temporary copies while preserving completed work.

- Replaced incomplete working copies when resuming loose-file preparation, while preserving completed work.

- Kept all parts of a complete MAME Software List cassette set together in one correctly named ZIP.
- Identified the affected MAME Software List archive when conflicting output prevents collection planning, while preserving existing files.

- Resumed at the stage where processing stopped after checking saved progress, required earlier results and collection folders, without rerunning completed stages.
- Offered Resume only when the saved run is consistent and unfinished, with a clear explanation when it cannot continue.

- Kept routine database checks out of the run-start display while leaving warnings and errors visible.
- Treated Cancel at the recovery menu as a cancellation without showing an additional failure message.

- Allowed processing to continue when a log file is briefly busy; a file that remains unavailable can still stop the run.
- Kept repeated notices about saved or unchanged incomplete sets out of the progress display, while retaining details in the log and duplicate totals in the final summary.
- Cleared temporary working files more quickly and reported when cleanup could not finish.
- Used Cracked as the folder label for recognized cracked variants in newly planned output.

- Reduced delays when saving the final catalogue while preserving the ability to resume interrupted work.

- Retried to open the collection database up to five times when access is temporarily unavailable, with a 00:00:10 pause between attempts and a clear message if access cannot be restored.

- Resumed an interrupted scan from the Organize menu without rerunning File Discovery or clearing existing output.

- Kept fuller failure details in stage logs, including errors during startup and file checking.
- Saved error details to an emergency log when normal logs are unavailable, and warned when no log could be written.

- Kept unidentified optical disc images together under Unknown File instead of unrelated review folders.
- Excluded only zero-byte files named exactly `_` as placeholders.
- Routed recognized alternate editions into a single Alternate Dumps folder without treating alternate status alone as an unofficial release, while preserving internal member directories inside ZIPs.
- Placed single-file Beta and Unlicensed releases in the appropriate unofficial folders when that information is available in the selected DAT. Existing recognized classifications take priority.

- Cleared previous output before a new Clear run starts, preventing old output from causing unnecessary Conflicts folders.
- Preserved completed output when resuming an interrupted Clear or Append run.
- Stopped final output when completeness checks find blocking issues, and reported the stopped run accurately.
- Summarized scan-preparation warnings on screen, keeping individual file details in the logs, and avoiding misleading messages when an archive was processed successfully.
- Fixed a completed preparation resume that could prevent collection planning from continuing.
- Placed games, applications and other recognized software categories in their corresponding format folders, including Atari 8-Bit and Atari ST, while avoiding unnecessary Conflicts folders for different formats of the same title.

- Corrected company and platform folders, including American Laser Games and ColecoVision, while keeping existing collection folders and package contents.

- Corrected game names in supplied GameBase DATs that contain characters unsuitable for filenames.
- Reused unchanged DAT discovery results when repeating discovery.
- Recognized ZIPs already created when resuming an interrupted Append run.
- Read more DiscJuggler CDI layouts, including mixed audio/data tracks and multiple sessions, while retaining the original input images.
- Checked converted tracks and disc layout before accepting the files, and stopped conversion when required disc information cannot be preserved.
- Produced CHD files for supported complete optical images, keeping Jaguar CD sets in ZIP packages and preserving existing RVZ files.
- Kept an unidentified converted disc together under Unknown File instead of sending its tracks and descriptor to separate review files.
- Recognized a complete CHD disc from its matching tracks without requiring a separate descriptor beside the original CHD.
- Kept single-disc games out of Incomplete Sets when their complete disc is present; reserving optical incomplete-set routing for identified sets missing whole discs.
- Prevented a track shared by several games from giving a whole disc the name or region of another game.
- Preserved track positions and the high-density boundary when converting GDI images to CHD and extracting them again.
- Recognized complete Redump Sega Naomi disc sets and produced CHD files with the names from the DAT.
- Accepted DATs with optional game identifiers without adding those identifiers to output filenames.
- Recognized Redump DATs that use either redump.info or redump.org source information.
- Removed duplicate complete sets according to your source preferences while keeping different sets that share some files.
- Avoided missed matches caused by hidden files, unusual filenames or file extensions.
- Kept progress displays stable and reduced repeated completion messages.
- Read file sizes correctly across supported DAT formats.
- Corrected GoodTools Atari 2600 set names to match their ROM filenames without the extension.
- Avoided unnecessary Conflicts folders when different DATs describe identical content, including filenames that differ only in letter case.
- Avoided uncertain matches caused only by an omitted optional MD5 checksum in a DAT.
- Kept unidentified archive members separate and added numbered suffixes within their review folders when filenames collide. Ordinary files without an extension remain under Unknown File.

### Known limitations

- Saving progress can fail after a stage finishes, stopping the run and leaving its saved completion status behind the completed work.

- Completeness is a property of the selected DAT set, not of an entire game. A DAT may describe each disk as a separate complete set. Having every listed member does not establish that every disk, edition or companion file needed to play the game is present. Whole-game estimates are informational and do not determine output placement.
- Incomplete-set handling remains limited: sets with missing required DAT members remain separate under Incomplete Sets. Whole-game completeness is not determined automatically. Completed ZIPs accumulated through Append are not automatically moved into the normal collection.

- Working files must remain unchanged after scan preparation; repeat preparation if they are edited or replaced.

- Not every operating system or revision can be identified. Operating System folders currently depend on the Operating Systems category in TOSEC DATs. Revisions require a recognized revision label; a version number alone does not qualify.
- Incomplete or uncertain media may be sent for review. Completeness checks depend on the available DAT information and cannot establish whether files omitted from a catalogue are required or whether a game is playable.
- MAME software-list disc support is incomplete. Sets combining ROM files and disc images cannot currently be processed together.
- CDI support is limited to certain disc layouts. Some images may not convert correctly, and successful conversion does not guarantee that a game will run in an emulator or on original hardware.
- Some NRG images cannot be converted because of unsupported disc information. MDS images cannot be processed if their companion data file cannot be opened. Audio differences are not repaired automatically.
- Copying existing RVZ files does not mean new RVZ files can be created. Conversion and recovery support remains limited.
- Locked platform files may produce a generic error. Close the program holding the file before repeating preparation.

- Keep the Incomplete Sets folder and its contents in place. Later Append or Resume processing that needs a recorded archive stops if it is missing; recreating an empty folder is insufficient.

## v2.0.0-beta.5 - 2026-09-11

### Added

- Added separate ZIPs for supported disk and tape images, with each file keeping
  its DAT filename. When a required file is missing, the available images go into
  separate ZIPs under NeedsAttention and the set remains incomplete.
- Added startup README pages that fit the console window, with final acceptance
  requested after the last page.

### Changed

- Reduced the time needed to create ZIP archives and copy files into the collection.

- Changed authority preference so supplemental A8P follows Atarimania, with
  MAME software lists following A8P and preceding Other.
- Removed the two Atari 2600 HyperList files from the recommended DAT sources.
- Removed the bundled CURATOR-created Atari 8-bit Family Atarimania GameBase
  2021 DAT because its file information could not be verified against its source.
- Updated the administrator, user, quick-start and API guides to explain current
  naming, repeated additions, removable review output, and current archive-writing and recovery behavior.

### Fixed

- Completed the separate chdman source package with three upstream FLAC test fixtures omitted from the previous source asset. The bundled binary is unchanged.

- Fixed processing after the needs_attention folder or its files have been removed, so review output can be created again.

- Fixed name collisions that created incorrect AlternateFormats folders, while
  keeping files in their configured platform and region locations.
- Fixed filename capitalization to retain spellings such as RealSports and
  CX2685 when a matching reference filename is available.
- Fixed ordinary collection ZIP capitalization while preserving recognized
  identifiers and spelling from supported reference DATs.
- Fixed repeated additions of copied files and ZIPs so matching outputs can be
  reused and different contents are kept separately.
- Fixed quoted DAT filenames being mistaken for fields such as file size.
- Fixed repeated CUE-check completion messages with grouped progress updates.
- Fixed Matching failures caused by unrelated DAT files sharing a filename,
  while retaining rejection of ambiguous sources when actually requested.

- Fixed long delays during collection completeness checks and adding clearer progress announcements.

- Fixed long delays when Organizer finishes publishing the collection.
- Fixed resume to stop when previously written files have changed.
- Fixed interrupted additions so valid newly created ZIPs can be recovered without being mistaken for older files.

- Fixed MAME software-list set titles to use their descriptions instead of
  abbreviated software identifiers.
- Fixed excessive per-file console messages in Completeness and Organizer while
  retaining their details in stage logs.
- Fixed publication ZIP and incomplete publication folder names to use the
  DAT's set name.
- Fixed detection of DolphinTool at the configured location.
- Fixed completeness reports so a missing or incorrectly sized required output
  prevents the set from being counted as complete.
- Fixed generated GameBase set names by removing added ID suffixes and trailing
  spaces.
- Fixed Atari 5200 DAT entries so alternative versions are separate sets.
- Fixed Atari Lynx DAT requirements to exclude readme files.
- Fixed missing Atari ST Automation and D-Bug entries in the bundled DAT.
- Fixed duplicate handling so a shared source file remains available for every
  required output.
- Fixed file verification information for unmatched CHD and CDI files sent for
  review.
- Fixed processing and reporting when no files qualify for the permanent
  collection.
- Fixed output filenames and filenames inside ZIPs to follow the DAT while
  keeping set titles separate.
- Fixed ZIP collisions so sets needing different member filenames retain
  separate packages. Packages with matching content but different member names
  use a Duplicate folder within the collection; different contents use separate
  Conflicts folders.
- Fixed repeated company and platform names, source labels, and duplicated
  format folders in output paths.
- Fixed incomplete publication packages being counted as complete.
- Fixed distinct DAT sets being lost when they share files or names. Sets remain
  separate whenever their complete definitions differ, including filename
  capitalization.
- Fixed collection reports to count each fulfilled DAT set correctly when files
  are shared between sets.
- Fixed experimental MAME SPLIT handling to keep parent, clone, BIOS, and device
  files with their required sets and flag missing dependencies.
- Fixed experimental MAME software-list file-size checks so undersized files
  are not accepted as complete.

### Known Limitations

Every BETA release requires a clean run; earlier databases, saved run state and output plans are incompatible. MAME support remains VERY EARLY and experimental; continue using clrmame as the definitive MAME ROM manager. Media conversion and broader recovery scenarios remain subject to open acceptance work.

## v2.0.0-beta.4 - 2026-09-03

### Added

- Added the officially identified CURATOR-modified MAME chdman build with
  `hashcd`, extraction-time logical-track evidence, preserved standard commands,
  full attribution, GPL-2.0-or-later notices, and explicit unofficial and
  non-affiliation identification.
- Added the required version-matched complete corresponding-source release
  asset and checksum, plus permanent GitHub publication instructions.
- Added persistent incremental Stage 1 and Stage 2 source ledgers, direct
  HyperList menu XML ingestion, and the CURATOR-created Atari ST Atarimania
  GameBase authority DAT.

### Changed

- Changed Stages 1-3 to reuse unchanged established authority, process only
  added or changed sources, retain absent-source authority additively, and
  preserve later collection state when authority is refreshed.
- Changed Stage 5 to use compact hash-addressed workspace roots, extract each
  CHD once, and consume exact emitted-track hashes from that extraction pass.
- Improved indexed relational hydration and bounded progress across Stages 1-3,
  Assembly, Completeness, and Reporting without changing authority results.
- Changed populated-output Full Runs to default to Append while retaining an
  explicit, doubly confirmed Clear choice.

### Fixed

- Fixed modified chdman hashing so Size, CRC32, and SHA-1 describe exactly the
  emitted split-track bytes and exclude non-emitted virtual pregap sectors.
- Fixed repeated Organizer-recovery prompts by retiring the exact discarded
  execution attempt transactionally.
- Fixed authoritative recovered-CUE reconciliation so obsolete unmatched-CUE
  review records are suppressed only after complete non-CUE identity proof,
  while genuinely unresolved sources remain for review.
- Fixed the Atari 8-bit Atarimania GameBase authority DAT by removing inherited
  archive-directory prefixes from ROM names while retaining valid catalogued
  non-ROM members and their exact identities.
- Fixed Stage 10 `Output Totals` ordering so `Unofficial` appears directly below
  `Official`, without changing any totals or execution behavior.
- Fixed configuration authority, clean database initialization, Nuclear Option
  documentation protection, run-state locking, legacy CHD classification,
  direct valid-CHD copying, collection lifecycle gating, and several authority,
  CUE, NeedsAttention, and reporting edge cases.
- Corrected all current operator guides to match the application’s actual path,
  source-preservation, recovery, configuration, and Stage 10 behavior.

### Known Limitations

- Some otherwise valid Alcohol MDF/MDS images may be incompatible with the
  bundled decoder; CURATOR preserves those sources and routes them for review.
- This is a beta release. Operators should use copied input, retain backups, and
  verify curated output before replacing original material.

## v2.0.0-beta.3 - 2026-08-27

### Added

- Added five CURATOR-created Atarimania GameBase authority DATs for Atari 2600,
  Atari 5200, Atari 7800, Atari Lynx, and Atari Jaguar.

### Changed

- Added explicit nested-archive lineage and content-only DAT freshness.
- Changed matching to universal raw-first authority selection without filename
  or extension inference.
- Routed NeedsAttention output by authoritative media category and improved
  truthful Assembly, Matching, recovery, publication, and manifest progress.
- Changed Stage 10 plan loading and permanent publication to bounded, set-based
  database operations.

### Fixed

- Fixed Windows-invalid A8P filenames without changing content identity.
- Fixed Stage 9 NO-GO sequencing and direct Stage 10 rejection.
- Fixed structural CUE materialization at the published authority-provenance
  boundary.
- Fixed full-run Append by retaining generation-owned physical-output evidence
  and allowing new plan entries while verifying every prior output by size and
  SHA-256.

### Known Limitations

- MAME support remains limited and preliminary and does not replace a dedicated
  MAME ROM manager.
- Some otherwise valid Alcohol MDF/MDS images may be incompatible with the
  bundled decoder; CURATOR preserves those sources and routes them for review.
- This is a beta release. Operators should use copied input, retain backups, and
  verify curated output before replacing original material.

## v2.0.0-beta.2 - 2026-08-25

### Added

- Added content-based Atari 8-bit Preservation and Atarimania GameBase
  authority profiles, plus the verified Atari Lynx Dragnet supplemental DAT.
- Added shared Core-owned Redump CUE recovery and official MAME software-list
  XML authority with matching-release DTD validation.
- Added database-backed permanent collection manifests, retained reporting
  history, and explicit Standard, Full Audit, Reconcile, and Detailed Export
  reporting actions.
- Added Reporting announcements for new permanent collection items, including
  platform breakdowns.

### Changed

- Added the three individually allowlisted CURATOR-created authority DATs to
  every public release while retaining empty operator-managed DAT surfaces.
- Replaced supported VerifyDump execution with CURATOR's faster deterministic
  unanimous native CHD/CUE resolver while retaining compatibility database
  structure and the protected dormant executable.
- Reused unchanged relational DAT authority through content-bound SHA-256
  fingerprints and fail-closed Core.Database transactions.
- Retained permanent authority-first Matching and set-first Assembly indexes,
  refreshed bounded SQLite planner statistics, and used authoritative set
  identity for multi-member completeness classification.
- Routed stage path handling and bounded leading-text reads through
  Core.Secondary, clarified NeedsAttention counts and source-identity
  vocabulary, and optimized Organizer Append verification using complete
  Core-owned physical-output evidence.
- Published every authoritative platform membership for exact raw
  cross-platform hash collisions and added offset-aware cartridge-header
  normalization.
- Derived Reporting results from permanent database records and clarified
  long-running Organizer and Reporting console operations.
- Clarified README and Developer Handbook MAME scope language: supported
  software-list XML supplies exact ROM/CHD authority, while complete
  dependency-aware MAME collection management remains outside CURATOR's scope.

### Fixed

- Fixed exact authority-ID reconciliation, CUE-source existence validation,
  case-distinct DAR sets, repeated member occurrences, and recovery of one exact
  missing authoritative CUE descriptor.
- Fixed MAME hexadecimal size canonicalization and changed-authority
  replacement, incomplete CUE-set completion, and unresolved NeedsAttention
  archive destination routing.
- Fixed Atari Lynx and Atari 7800 header validation, Stage 5 missing-CUE
  publication and loose-file SHA-1 initialization, and zero-new-item manifest
  reporting.
- Fixed Organizer Append duplicate totals, duplicate NeedsAttention physical
  planning, and authority-driven output classification independent of source
  provenance.

### Known Limitations

- MAME support remains limited and preliminary and does not replace a dedicated
  MAME ROM manager.
- Some otherwise valid Alcohol MDF/MDS images may be incompatible with the
  bundled decoder; CURATOR preserves those sources and routes them for review.
- This is a beta release. Operators should use copied input, retain backups, and
  verify curated output before replacing original material.

## v2.0.0-beta.1 - 2026-08-21

### Added

- Added capability-based Bootstrap initialization through validated static call
  sheets and on-request Core activation.
- Added the persistent SQLite authority database and relational contracts used
  by Stages 1-10 and Reporting.
- Added pinned Microsoft.Data.Sqlite, SQLitePCLRaw, and native SQLite runtime
  dependencies, together with integrity and provenance records.
- Added complete output receipts, company manifests, placement evidence,
  recovery state, and collection-audit workflows.

### Changed

- Replaced the heavy in-memory crunching paths in Stages 6-9 with indexed,
  set-based SQLite operations while retaining physical file work in Core-owned
  services.
- Changed Stage 10 to execute a frozen relational plan with durable receipt
  checkpoints, resumable publication, verified Append reuse, and optimized
  final cleanup.
- Changed Gateway startup to draw the console header before Core initialization,
  present Core readiness as numbered steps, and request only the capabilities
  needed by the selected action.
- Improved end-user announcements and truthful progress across Gateway,
  numbered stages, Reporting, cleanup, database loading, and publication.
- Updated all current guides, legal notices, attribution, dependency records,
  component identities, and public-release protections for CURATOR
  `v2.0.0-beta.1`.

### Fixed

- Fixed Gateway option 8 so pause-enabled runs pause after each successful stage
  summary without changing the established behavior of options 4 and 6.
- Fixed unresolved archive review output to retain top-level source lineage and
  preserve nested member paths without collisions.
- Fixed Stage 5 missing-source handling, Stage 7 relational validation scaling,
  optical CUE membership reconstruction, and several silent console intervals.
- Fixed authorized cleanup and Stage 10 workspace cleanup to avoid redundant
  enumeration while preserving failure evidence and required folder surfaces.

### Known Limitations

- MAME support remains limited and preliminary and does not replace a dedicated
  MAME ROM manager.
- Some otherwise valid Alcohol MDF/MDS images may be incompatible with the
  bundled decoder; CURATOR preserves those sources and routes them for review.
- This is a beta release. Operators should use copied input, retain backups, and
  verify curated output before replacing original material.

## v1.0.0-beta.8 - 2026-08-13

### Added

- Added the six managed Aaru libraries used for in-process CDI, NRG, and
  MDF/MDS decoding while preserving original source custody and continuing
  unsupported images through the normal review path.
- Added exact content-authoritative Redump CUE resolution for configured
  optical platforms, including Atari Jaguar CD authority data.
- Added exact `AuthoritySetId` collector-platform overlays, including Sega CD
  32X presentation, without changing DAT platform authority.
- Added the output-wide receipt manifest used to validate deterministic Stage
  10 Append reuse by destination, size, SHA-256, record fingerprint, and
  complete manifest fingerprint.

### Changed

- Stage 1 now uses Core-owned bounded DAT leading-text reads and throttled
  progress rendering. Stage 2 reuses its fail-closed platform association.
  Stages 3 and 4 use indexed, batched, and single-pass construction paths that
  preserve their established output contracts.
- Stage 5 captures Size, CRC32, and SHA-1 during extraction or copying, reuses
  complete persisted identity evidence, performs bounded CHD extraction, and
  retains Core-owned fallback reads when trustworthy evidence is unavailable.
- Stage 6 trusts the completed Stage 5 handoff, reports checked and reused
  identities accurately, and reuses immutable matching evidence without
  weakening content-only authority.
- Stage 7 validates immutable upstream identity through keyed authority
  lookups without rehashing. Stage 8 uses a per-set keyed lookup for exact
  shared-source evidence. Stage 9 uses keyed destination collections while
  preserving collision handling and exact Stage 10 instruction order.
- Optical CUE correction is now last resort after ordinary prepared-hash,
  normalization, sibling, and exact/profile-compatible repository workflows.
  Complete optical sets with one safely derived structural CUE remain eligible
  for Official output only when every non-CUE membership is present and exact;
  the descriptor discrepancy remains explicit evidence.
- Core API documentation now covers 149 interfaces. Current operator guides
  describe the Stage 9 execution contract, output-wide receipt, company
  manifests, structural-CUE eligibility, and current component identities.

### Fixed

- Fixed non-Redump structural CUE handling so a missing same-named Redump
  member falls through instead of aborting Matching; ambiguity and conflicting
  repository evidence still fail closed.
- Fixed a concurrent Core.Progress queue race that could terminate otherwise
  valid stage work while preserving TaskBar ordering and caller contracts.
- Fixed publication packages whose distinct authority entry names share exact
  physical content, while retaining strict non-publication and optical
  membership rules.
- Fixed configured non-set files (`.txt`, `.exe`, `.dll`, and `.bat`) entering
  Needs Attention output and corrected authoritative Jaguar CD CUE handling.

### Known Limitations

- Reporting can classify the root receipt manifest as unmanifested content;
  investigation remains deferred under `DEFERRED-053`.
- Stage 3/5 progress-presentation tracing, the Stage 6 prebuilt DAR index and
  output-publication investigation, and the distinction between upstream
  content identity and final copied-artifact evidence remain deferred under
  `DEFERRED-055`, `DEFERRED-045`, `DEFERRED-057`, and `DEFERRED-059`.

## v1.0.0-beta.7 - 2026-08-08

### Changed

- Stage 3 reuses its already-computed incoming company summary after a
  conflict-free merge only when platform, DAT, membership, and merge-accounting
  checks prove that it exactly describes the complete published company DAR.
  Every non-equivalent or conflicting case retains the full fail-closed summary
  reconstruction path.
- Stage 9 now publishes the complete ordered schema-1 physical-output
  execution contract, including stable identities, exact destinations,
  packaging, source relationships, cleanup ownership, and manifest authority.
- Stage 10 now consumes the Stage 9 execution contract directly and no longer
  reconstructs naming, routing, grouping, ordering, collision, or manifest
  decisions from historical records.
- Append now requires a valid output-wide receipt manifest and matching
  physical size/SHA-256 evidence before an existing target may be skipped.
- Stage 10 publishes a deterministic output-wide receipt manifest.

- DependencyIntegrity now validates the manifest-level redistribution policy
  and every entry's redistribution metadata.
- Completed `DEFERRED-038`: confirmed the bundled Binmerge executable as the
  publisher's exact 1.0.3 Windows release asset and identified the eleven
  Redump cue/GDI metadata archives as public-domain metadata. The manifest
  preserves the retired historical-endpoint limitation for three GDI archives.
- The Core API handbook now documents 146 current interfaces, including the
  Core.Primary dependency-path resolver used by DependencyIntegrity.

### Fixed

- Removed superseded Stage 10 planning and authority-reconstruction paths.
- Completed a fresh live Stages 1-11 validation. Organizer produced 24,269 of
  24,269 planned unique outputs with zero failures. Independent receipt checks
  found zero missing paths, size mismatches, or SHA-256 mismatches, and every
  output-wide and company-manifest fingerprint validated.

- Completed `DEFERRED-051`: Reporting now excludes `needs_attention`
  filesystem content and NeedsAttention manifest rows from every authoritative
  collection boundary, including reconciliation, audits, caches, ledgers,
  diagnostics, viewers, and publication.
- Reconciled current operator guides, component build indexes, source module
  identity, and the release inventory with the validated August 7 workspace
  baseline.

### Known limitations

- Reporting classifies the administrative root receipt manifest
  `00_Manifest\CURATOR_Output_Manifest.json` as unmanifested collection
  content. Collection paths, sizes, hashes, and fingerprints remain valid;
  the reporting-boundary investigation is tracked as `DEFERRED-053`.

## v1.0.0-beta.6 - 2026-08-04

### Changed

- Complete Atari Jaguar CD authority sets now publish as ZIP, while complete
  optical authority sets for every other platform publish as CHD. Source
  container type no longer determines final optical format.
- CUE normalization now occurs universally after final DAR membership and
  authoritative naming are resolved. Organizer consumes that resolved contract
  without repairing or reinterpreting it.
- Successful ZIP and CHD creation is accepted from the owning creation
  operation. Production stages no longer reopen successful output for
  verification.
- Reporting remains focused on manifests, physical paths, sizes, and requested
  fingerprints; archive formats, CUE contracts, and CHD structure remain owned
  by producing stages.

### Maintenance

- Removed 14 proven-unreachable private functions and 566 stale implementation
  and comment lines.
- Shortened 15 private functions and 31 private/local variables to CURATOR's
  established concise internal naming convention without changing public APIs,
  contracts, schemas, component builds, or runtime behavior.

### Validation

- Completed Stages 1 through 10 individually and completed Reporting through
  the visible execution path.
- Organizer produced 7,334 of 7,334 outputs with zero failures.
- Reporting matched all 4,775 authoritative manifest fingerprints, and an
  independent physical audit matched all 4,785 authoritative payload entries
  to exact DAR membership, case-sensitive names, sizes, CRC32, and SHA-1.

### Known limitations

- Reporting_DEV_53 still processes `needs_attention` filesystem content and
  NeedsAttention manifest rows. Complete exclusion remains unresolved under
  `DEFERRED-051`.
- Dependency provenance and redistribution-policy validation remain open under
  `DEFERRED-038`.

## v1.0.0-beta.5 - 2026-08-03

### Changed

- Reporting now presents collection work as concise operator-facing phases
  while retaining detailed technical milestones in DEBUG logs.
- Full physical-audit reconciliation now uses bounded summary and individual
  review panels with explicit Approve All, Review Each, Make No Changes, and
  Cancel consequences. Only approved findings alter authoritative manifests.
- Published guides now distinguish the intended collection boundary from
  beta.5 behavior: authoritative collection truth is official plus unofficial
  physical output, while `needs_attention` is intended to remain a separate
  review queue.

### Fixed

- Preserved original and immediate Reporting publication provenance across
  repeated transitive reuse so valid unchanged reports remain current.
- Preserved complete multi-member DAR sets spanning multiple source containers
  during Stage 9 set planning.
- Corrected Core API handbook metadata so the application version is not
  presented as the Core.ApiDocumentation component build.

### Known limitations

- Reporting_DEV_49 in beta.5 still processes `needs_attention` filesystem
  content and NeedsAttention manifest rows through classification, counting,
  summaries, and presentation. Complete exclusion remains unresolved under
  `DEFERRED-051`.

## v1.0.0-beta.4 - 2026-07-31

### Added

- Added `END_USER_LICENSE_AND_LEGAL_NOTICE.md` as a required release
  deliverable. It supplements the GNU GPL with CURATOR-specific no-warranty,
  assumption-of-risk, limitation-of-liability, backup, content-responsibility,
  third-party, trademark, modified-release, and support notices without
  restricting GPL-granted rights.
- Added schema-v2 company manifests with final-artifact SHA-256 evidence and
  immutable existing-record behavior during Append.
- Added Gateway option `V` for an explicit full physical SHA-256 collection
  audit with operator-reviewed manifest reconciliation.

### Fixed

- Suppressed internal `latest_status.json` read messages so refreshed Gateway
  menus and confirmation screens start with a clean application header.
- Corrected Stage 7 validation of contextual CHD/CUE authority matches so
  current `AuthorityProvenance` DAT evidence is accepted without weakening
  missing-evidence or authority-integrity checks.
- Closed the selected-run pause correction after operator confirmation of the
  remaining acknowledgement-order paths.

## v1.0.0-beta.3 - 2026-07-30

### Changed

- Added a standalone `LICENSE` file containing the complete GNU General Public
  License version 3 text.
- Stage 5 now reports exact, visible progress while classifying and verifying
  large source inventories before preparation begins.
- Stage 6 now reports exact file counts while hashing, preparing matching
  results, serializing records, and verifying output bytes.
- Stage 6 reduces unnecessary console rendering during large matching runs
  while preserving matching results, integrity verification, recovery
  behavior, and atomic JSON publication.
- Stage 7 removes repeated validation scans and reports exact progress while
  validating authority files and publishing its six output collections.
- Stage 8 reuses validated authority membership data instead of rebuilding it,
  removes repeated assembly scans, and reports exact progress through source
  preparation, collection assembly, review routing, and final publication.
- Large Stage 8 assembly runs now complete substantially faster while
  preserving the same normalized collection result.
- Stage 9 reports exact progress across decision planning and final
  publication while avoiding redundant routing, receipt, and source-path
  preparation.
- Stage 10 trusts the accepted Stage 9 inventory, validates planned sources
  lexically beneath authorized roots, and leaves missing-source detection to
  the physical operation that consumes each source.
- The End User Manual and Quick Start Guide now explain that CURATOR does not
  provide complete MAME-native ROM-set management and recommend current
  `clrmame` for that work. The established legacy `clrmamepro` remains
  available.

### Fixed

- Fixed long Stage 8 intervals that previously had no visible console
  reporting.
- Fixed the Stage 8 final JSON progress display so it reflects the stage's
  selected membership and review records before verifying output bytes.
- Added the missing blank line above the final stage resource-release message.
- Adjusted selected pause-enabled Gateway options 4, 6, and 8 to suppress a
  redundant post-summary pause while retaining their summary and final Gateway
  acknowledgement.
- Regenerated the Core API Developer Handbook so its opening safety notice
  renders headings and emphasis normally.
- Corrected the End User Manual cover to identify `v1.0.0-beta.3` and the
  current document-update date.
- Removed Stage 10 planning-time source existence probes and the large
  source-tree preflight without changing the accepted output plan or
  destination safety checks.

### Known limitations

- Dependency integrity hashes do not complete provenance or redistribution
  review. The exact bundled Binmerge build and redistribution evidence for
  eleven cue/GDI ZIP packages remain unresolved under `DEFERRED-038`.
- The selected-run pause correction is implemented, but the complete
  `DEFERRED-046` acknowledgement-order matrix remains unproven across paused
  and non-paused Full Run, single-stage, Run From Stage, Run Through Stage,
  failure, cancellation, and noninteractive paths.

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

