# CURATOR v2.0.0-beta.3 Changelog

Last updated: August 27, 2026

This changelog summarizes new features, improvements, fixes, and known
limitations in each CURATOR release.

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

- Added limited, preliminary ingestion of content-validated MAME `-listxml`
  exports for coin-operated Arcade ROM and CHD authority. Recognition uses the
  MAME XML contract rather than requiring a filename prefix.
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

- Stage 3 authority-set identity now includes the canonical DAT key rather than
  relying on a physical DAT filename. DAR publishes that key through provenance
  and keeps distinct authoritative DAT identities stable across file renames.
- MAME Arcade publication now uses split-set membership: machine-owned ROMs
  remain with each machine while parent, BIOS, and device dependencies remain
  separate sets. MAME internal CHD SHA-1 authority takes precedence over
  Redump-derived optical-track evidence on the MAME path.
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

- MAME support is limited and preliminary. It covers coin-operated Arcade
  entries from validated `-listxml`, excludes `nodump`, and routes incomplete
  authority sets to NeedsAttention. It does not provide merged, non-merged,
  standalone, software-list, or general non-Arcade MAME management; validate
  results with the intended MAME release or current `clrmame`.
- Reporting can classify the root receipt manifest as unmanifested content;
  investigation remains deferred under `DEFERRED-053`.
- Stage 3/5 progress-presentation tracing, the Stage 6 prebuilt DAR index and
  output-publication investigation, and the distinction between upstream
  content identity and final copied-artifact evidence remain deferred under
  `DEFERRED-055`, `DEFERRED-045`, `DEFERRED-057`, and `DEFERRED-059`.

## v1.0.0-beta.7 - 2026-08-08

### Added

- Stage 5 now attempts in-process decoding of supported CDI, NRG, and MDF/MDS
  optical images into deterministic raw long-sector track members for ordinary
  exact-hash matching. Original sources remain intact; decoder failures are
  logged and continue through the standard review workflow.
- CURATOR now bundles the six managed Aaru libraries required by that optical
  decoding boundary. No separate Aaru executable, configuration, database, or
  PATH setup is required.
- Stage 5 now records Size, CRC32, and SHA-1 for every prepared file and
  publishes deterministic CUE-reference custody evidence for ZIP, loose-file,
  and CHD-derived media.
- Stage 6 reuses the Stage 5 content identity where normalization is not
  required. Optical authority selection remains content-only in the strict
  Size, CRC32, SHA-1 sequence; filenames never select DAT authority.
- CUE reference repair now works across prepared optical media. Physical
  references bind by FileID where possible, deterministic same-scope order is
  used only under complete unanimous set evidence, and rewritten CUE files
  receive authority only when their final content identity exactly matches the
  DAT member.
- Stages 7–9 now preserve a corrected but non-authoritative CUE as a structural
  descriptor, keep incomplete optical sets incomplete, and emit one complete
  Needs Attention set without duplicating the CUE.

### Fixed

- Prevented duplicate physical sources from satisfying multiple authority
  memberships in an optical set.
- Removed filename-based CHD member and set scoring that could override
  content identity.
- Corrected ZIP-origin and loose-file-origin CUE handling so mismatched track
  references are repaired deterministically without promoting an inexact CUE
  to DAT authority.

### Changed

- TaskBars now default to numeric counts, preserve genuinely empty detail,
  coalesce superseded queued frames, and suppress regressive display updates
  without interrupting stage work. Per-item and per-phase row generations keep
  legitimate transitions monotonic. Stage 2 no longer presents an unknown XML
  set total as complete, and Stage 9 retains continuous progress through final
  publication.

- Stage 6 now obtains an authoritative optical CUE only after BIN content
  uniquely resolves the DAT set. It copies the exact DAT-named CUE from the
  configured Redump archive, verifies Size, CRC32, and SHA-1, and proves the
  source archive unchanged by pre/post SHA-256. The slower VerifyDump path and
  prior CUE-repair path are disabled by default. Repeated TestBed Stages 5-10
  matched 33 of 33 members and produced 11 official CHDs with zero Needs
  Attention records in 40-42 seconds for Matching.

- Stage 3 company-DAR reconciliation now batches Core-owned deterministic JSON
  comparisons and replaces matched metadata records by their indexed saved
  position instead of repeatedly scanning the complete saved DAT. A forced
  6,931-entry merge improved from 15 minutes 16 seconds to 16 seconds, and
  full 83-DAT validation preserved the pre-optimization 99.4 MB company DAR
  byte-for-byte while retaining all authoritative and context-lineage records.
- Stage 3 now caches repeated authoritative set hashes, while Core.Secondary
  reuses synchronized provider-owned text-hash state. Repeated TestBed runs
  improved from 101 seconds to 87 seconds with exact normalized DAR output;
  the complete Stage 2-10 and Reporting chain passed without hash or
  publication failures.
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
- All four published guides now identify the root output receipt and company
  manifests at the appropriate audience level. They warn that deleting or
  changing the root receipt breaks trusted Append continuity, while deleting
  or changing a company manifest compromises Reporting coverage for that
  company until valid evidence is restored.

- DependencyIntegrity now validates the manifest-level redistribution policy
  and every entry's redistribution metadata.
- Completed `DEFERRED-038`: confirmed the bundled Binmerge executable as the
  publisher's exact 1.0.3 Windows release asset and identified the eleven
  Redump cue/GDI metadata archives as public-domain metadata. The manifest
  preserves the retired historical-endpoint limitation for three GDI archives.
- The Core API handbook now documents 148 current interfaces, including the
  Core.Secondary deterministic comparison batch API used by Stage 3 and the
  managed proprietary optical-image decoding boundary used by Stage 5.

### Fixed

- Gateway collection-folder paths now display only the path root and final
  folder name, such as `C:\...\workspace`, instead of truncating arbitrary
  characters from the middle of the full path.
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
- Dependency provenance remains open under `DEFERRED-038`; redistribution-
  policy validation was completed after the beta.6 release.

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
- The eleven cue/GDI ZIP packages remain included under an explicit unresolved
  redistribution policy. Their manifest records retain unresolved licenses
  while adding `LicenseAssertion: NOASSERTION` and
  `RedistributionStatus: Unverified`; the legal and third-party notices state
  that inclusion does not establish redistribution permission.

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
