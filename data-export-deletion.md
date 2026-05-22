# Data Export and Deletion Policy

## Purpose

This document explains the intended export and deletion principles for the Human Performance Analytics Project.

The project is currently in development and evaluation phase.

## Data Export

Users should be able to export their data in a structured format.

Exportable data may include:

- normalized Garmin-derived metrics;
- activity summaries;
- import logs;
- data quality information;
- rejected-data quarantine logs;
- manually entered contextual data;
- nutrition logs;
- recipes;
- subjective wellness logs;
- training notes.

The preferred export format during development is JSON. CSV export may be added later for selected data categories.

## Data Deletion

Users should be able to request or perform deletion of their data.

Deletion may include:

- local data deletion;
- cloud-stored data deletion where applicable;
- deletion of manually entered contextual data;
- deletion of nutrition logs;
- deletion of activity-derived data;
- deletion of import logs;
- deletion of rejected-data quarantine logs.

## Garmin Access Revocation

If Garmin API integration is granted in the future, users should be able to disconnect Garmin access.

The system should stop future synchronization after access is revoked.

## Local-Only Data

Some sensitive data categories may remain local-only by default, such as:

- pain or discomfort notes;
- subjective wellness logs;
- nutrition details;
- menstrual data if implemented;
- private notes;
- voice transcriptions if implemented.

## Contact

For export or deletion requests, contact:

humanperformance.analytics@gmail.com
