# CURATOR Third-Party Dependency Record

CURATOR includes third-party libraries, executable tools, and cue-data
packages. Their exact packaged identities are recorded in
`config\dependency-manifest.json` and can be checked with
`scripts\DependencyIntegrity.ps1`.

An integrity match proves that a packaged file has not changed from the
recorded CURATOR distribution. It does not, by itself, establish source
provenance or redistribution permission.

## Current metadata status

- Known binary identities and unresolved metadata are recorded in the manifest.
  verifydump is publisher version 1.0.0, verified byte-for-byte against its official
  Windows release. Original component notices are retained under documentation/licenses.
  The packaged Binmerge executable exactly matches the
  publisher's Binmerge 1.0.3 Windows release asset at commit `7922719`.
- The cue/GDI ZIP packages retain their publisher-style filename dates,
  sizes, and SHA-256 identities. The manifest records publisher links and any limitations on verifying
  original archive hashes.
- Redump states that its stored metadata is public domain and may be used
  without restriction. The manifest records these packages as
  `LicenseRef-Redump-Public-Domain` and preserves the GDI evidence limitation.

## Packaged dependency groups

- Managed libraries: Aaru.CommonTypes, Aaru.Console, Aaru.Decoders,
  Aaru.Filters, Aaru.Helpers, Aaru.Images, AlphaFS, HashLib4CSharp,
  Microsoft.Bcl.TimeProvider, Microsoft.Data.Sqlite, Newtonsoft.Json,
  Newtonsoft.Json.Schema, SQLitePCLRaw.batteries_v2, SQLitePCLRaw.core,
  SQLitePCLRaw.provider.e_sqlite3, Spectre.Console.Ansi, and Spectre.Console.
- Native libraries: `7z.dll` and SQLite `e_sqlite3.dll`.
- External tools: binmerge, chdman, DolphinTool, verifydump, and retained 7z.exe.
- Data: platform-specific cue and GDI ZIP packages under `tools\cues`.

## License summary

- MIT: Aaru.CommonTypes, AlphaFS, HashLib4CSharp,
  Microsoft.Bcl.TimeProvider, Microsoft.Data.Sqlite, Newtonsoft.Json,
  and Spectre.Console.
- Apache-2.0: SQLitePCLRaw.batteries_v2, SQLitePCLRaw.core, and
  SQLitePCLRaw.provider.e_sqlite3.
- LGPL-2.1-only: Aaru.Console, Aaru.Decoders, Aaru.Filters, Aaru.Helpers, and
  Aaru.Images.
- AGPL-3.0 or purchased commercial license: Newtonsoft.Json.Schema.
- GPL-2.0-or-later: binmerge.
- GPL-2.0-or-later: CURATOR's modified MAME chdman build and DolphinTool.
- LGPL-2.1-or-later, the 7-Zip unRAR restriction, BSD-3-Clause, and BSD-2-Clause
  components: 7-Zip. The publisher's complete license notice controls and must
  accompany binary redistribution.
- Public domain: SQLite and Redump cue/GDI metadata archives.

## Copyright and project attribution

- Aaru: Natalia Portillo and Aaru project contributors. CURATOR modifications
  to Aaru.Images copyright © 2026 Miguel A. Ortiz; coding assistance by
  OpenAI ChatGPT. Original author notices and licenses remain intact.
- AlphaFS: Peter Palotas, Jeffrey Jangli, Alexandr Normuradov, and
  contributors.
- HashLib4CSharp: Ugochukwu Mmaduekwe and project contributors.
- Microsoft.Bcl.TimeProvider and Microsoft.Data.Sqlite: Microsoft and .NET
  Foundation contributors.
- Newtonsoft.Json and Newtonsoft.Json.Schema: James Newton-King and
  contributors.
- SQLitePCLRaw: Eric Sink, SourceGear, LLC, Microsoft Open Technologies, Inc.,
  and project contributors; bundled SQLite itself is dedicated to the public
  domain.
- Spectre.Console: Patrik Svensson, Phil Scott, Nils Andresen, Cédric Luthi,
  and contributors.
- 7-Zip: Igor Pavlov; its bundled BSD-derived portions retain the publisher
  notices for Apple Inc., Facebook, Inc., Yann Collet, and Alexander Roshal
  (original unRAR code). The complete publisher notice is packaged at
  documentation/7ZIP_LICENSE.txt.
- BinMerge: copyright © 2024 Chris Putnam and contributors. Its embedded
  Python 3.12.2 and OpenSSL 3.0.13 component notices are retained in
  documentation/licenses/PYTHON_3.12.2_LICENSE.txt; PyInstaller uses its
  published executable-bundle exception.
- Modified MAME chdman: MAMEDev and contributors; CURATOR logical-track
  hashing modifications copyright © 2026 Miguel A. Ortiz.
- DolphinTool: the Dolphin Emulator project and contributors.
- verifydump 1.0.0: copyright © 2022 j68k; MIT. The bundled executable exactly
  matches the publisher Windows release. Embedded CPython 3.10.4 retains Python
  Software Foundation, CWI, CNRI and BeOpen notices; PyInstaller 5.1 retains its
  GPL exception/Apache notices; OpenSSL 1.1.1n retains OpenSSL Project, Eric Young
  and Tim Hudson credit. Microsoft runtime components retain Microsoft credit.
  Complete original terms and incorporated-component acknowledgements are in
  documentation/licenses/PYTHON_3.10.4_LICENSE.txt and accompanying notices.

The precise license text and attribution requirements published by each
upstream project remain controlling. Source and package links for every
packaged artifact are recorded in `config\dependency-manifest.json`.

Redistributing GPL, AGPL, LGPL, or commercially licensed components can impose
requirements beyond attribution. The corresponding publisher terms and source
availability obligations must be satisfied by the distributor.

## Modified MAME chdman

`tools\chdman.exe` is CURATOR's unofficial modified build of MAME chdman. Its
identity is `0.289-CURATOR.8-poc`, as recorded by the current dependency manifest, from upstream
MAME commit `83b908c74253f7161455347379137a233cca1636`. It retains the standard
chdman command set and adds `hashcd`, streamed logical-track hashing with bounded
header prefixes, and optional extraction-time logical-track evidence. Scan
Preparation hashes decoded tracks without writing BIN files; applicable
normalization and pending output operations still extract tracks through Core.
Logical-track hashes describe the bytes emitted for each split track and do not
synthesize virtual pregap bytes absent from those files. The original CURATOR.5
build and its beta.5 compatibility identity remain historical provenance.

The complete binary is distributed under GPL-2.0-or-later. Each public release
containing it must provide the exact complete corresponding source as the
separate, version-matched asset `CURATOR_v<application-version>_chdman-source.zip`
and publish its SHA-256 checksum. Patches or links to upstream source are not a
substitute for that complete source package.

This is not an official MAMEdev build. It is not produced, sponsored, approved,
or supported by MAMEdev. MAME is a registered trademark of Gregory Ember; the
name is used only for accurate upstream attribution and compatibility
description. Upstream project and license information:
https://www.mamedev.org/ and https://docs.mamedev.org/license.html

Redump's publisher statement identifies its stored metadata as public domain
and available for use however people see fit. This applies to the packaged
CUE/GDI descriptors, not to referenced game content or third-party marks.

`tools\7z.exe` is retained in the current package inventory for traceability,
but it is not a required CURATOR runtime tool. All reachable CURATOR archive
operations use `tools\7z.dll`.

## Validation

From the CURATOR application root:

```powershell
pwsh -NoProfile -File .\scripts\DependencyIntegrity.ps1
```

The command exits unsuccessfully if a recorded file is missing or its size or
SHA-256 identity differs. Unresolved version, provenance, and license metadata
is reported separately and does not conceal an integrity failure.

This record is informational and is not legal advice. Original third-party
license terms remain controlling.

## CURATOR project and modified Aaru source

myOrganizer: CURATOR — Collection Utility for Retro Archive Tracking,
Organization, Repository — was created, architected and is managed by
Miguel A. Ortiz. Copyright © 2026 Miguel A. Ortiz. OpenAI ChatGPT provided
development, coding and documentation assistance. This does not transfer
project ownership or replace any upstream credit.

Aaru.Images 5.4.1-curator-poc1 is an unofficial modified build based on
upstream commit 06405f4976e44afcae20b9681ae367454829551a. It is not an official
Aaru release and implies no Aaru sponsorship or endorsement. Exact modified
source/build inputs, original license texts and attribution accompany
CURATOR_v2.5.0-beta.1_aaru-source.zip. Its BUILD_CURRENT_RELEASE.md and
SOURCE_BUILD_CREDITS.md identify the modification and retained build components.

## Authority and metadata projects

Packaged Atari authorities retain their embedded publisher credits: A8P,
Atarimania/GameBase contributors and Lynx Dragnet contributors. Other supported
authorities include No-Intro/DAT-o-MATIC, Redump, TOSEC, Libretro Database,
MAME, progetto-SNAPS and LaunchBox. Operator-selected inputs retain their
original authorship and notices. Names and trademarks remain with their owners;
mention implies no affiliation, sponsorship or endorsement.

## Corresponding source and licensing basis

This distribution uses Json.NET Schema 4.0.1 under its published AGPL-3.0
alternative; no purchased commercial license is asserted. Its original license
notice, complete AGPL text and exact pinned source are supplied. CURATOR retains
its GPL-3.0-or-later license; applicable combined-work obligations remain governed
by GPL/AGPL section 13. No application or dependency license text is rewritten.

See SOURCE_DISTRIBUTION.md for the matching source companion assets. License
texts, package metadata and incorporated dependency notices supplement concise
credits here. Offering binaries must also provide the corresponding source
assets with equivalent access.

The publisher advertises the free Json.NET Schema edition with a limit of
1,000 validations per hour. This limit belongs to the dependency; runtime
validation and CURATOR workload acceptance were excluded from this preparation.
