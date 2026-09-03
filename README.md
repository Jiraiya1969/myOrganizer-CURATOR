# myOrganizer: CURATOR

CURATOR is a Windows PowerShell application for analyzing, validating, reconstructing, and organizing emulation collections using DAT-based authority data.

The current public release is **CURATOR v2.0.0-beta.4**.

CURATOR v2 is a major architectural overhaul. It replaces the principal
in-memory processing paths with persistent, indexed SQLite authority,
execution, recovery, and audit workflows across Stages 1–10 and Reporting.
The v1 release line is closed and preserved as immutable release history; all
continuing development now proceeds exclusively under v2.

<p align="center">
  <img src="assets/images/branding/CURATOR_official_logo_concept_v2_bordered_reflective.png" alt="CURATOR official logo" width="520">
</p>

<p align="center">
  <img src="assets/images/branding/CURATOR_packaging_cover_concept_v2.png" alt="CURATOR preview artwork" width="720">
</p>

Copyright © 2026 Miguel A. Ortiz.

This notice covers the CURATOR project and its original artwork and branding;
the software remains available under the license described below.

---

## What is CURATOR?

Starting with user-provided source files, CURATOR prepares, validates, documents, and organizes every asset using trusted preservation metadata. Unknown, incomplete, and unsupported content is identified and separated so every decision remains transparent.

The result is a clean collection with a complete audit trail, making it easy to review, maintain, and update as preservation projects continue to evolve.

---

## How CURATOR Works

### 1. Authority Preparation

Prepare preservation DATs and supporting reference metadata before any collection work begins.

<p align="center">
  <img src="assets/images/workflow/01_retro_authority_preparation.png" alt="Authority Preparation" width="900">
</p>

### 2. Deterministic Matching

Evaluate every user-provided file against trusted preservation metadata to identify known content and separate unknown material.

<p align="center">
  <img src="assets/images/workflow/02_retro_deterministic_matching.png" alt="Deterministic Matching" width="900">
</p>

### 3. LaunchBox Organization

Organize verified content into a structured, LaunchBox-ready library while preserving relationships between source material, metadata, and output.

<p align="center">
  <img src="assets/images/workflow/03_retro_launchbox_organization.png" alt="LaunchBox Organization" width="900">
</p>

### 4. Reporting & Reconciliation

Document every action so collections can be reviewed, reconciled, and maintained as preservation projects evolve.

<p align="center">
  <img src="assets/images/workflow/04_retro_reporting_reconciliation.png" alt="Reporting & Reconciliation" width="900">
</p>

---

## Current Status

CURATOR is currently available as **v2.0.0-beta.4**.

This fourth v2 public beta adds the officially identified CURATOR-modified MAME
chdman build and its complete corresponding source, persistent incremental
Stage 1 and Stage 2 source ledgers, direct HyperList ingestion, compact CHD
staging, and the authority, recovery, progress, configuration, documentation,
and reporting corrections recorded in the changelog.

The closed v1 release line remains permanently available and will receive no
further development or release changes.

Download the current beta and verify its published SHA-256 checksum on the
[authoritative GitHub Release](https://github.com/Jiraiya1969/myOrganizer-CURATOR/releases/tag/v2.0.0-beta.4).

Every published version remains available in the
[public release archive](https://myorganizerhq.com/releases). See the
[project changelog](CHANGELOG.md) for improvements, fixes, and known
limitations in each release.

---

## Free & Open Source

CURATOR is free, open-source software licensed under the
[GNU General Public License v3.0 or later](LICENSE).

CURATOR-specific warranty, liability, safety, content-responsibility,
third-party, trademark, modified-release, and support notices are provided in
the [End User License and Legal Notice](END_USER_LICENSE_AND_LEGAL_NOTICE.md).

---

## Safety Notice

CURATOR reorganizes, stages, extracts, packages, and writes files.

Always work from copies of your original data and review generated output before replacing existing collections.

---

## Contact

Questions, feedback, bug reports, and project discussions are welcome.

**Website:** https://myorganizerhq.com

**Email:** contact@myorganizerhq.com

**Repository:** https://github.com/Jiraiya1969/myOrganizer-CURATOR
