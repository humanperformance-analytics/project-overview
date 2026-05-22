# Technical Architecture

## Overview

Human Performance Analytics Project is designed as a consent-based analytics platform for Garmin-authorized data and manually entered contextual information.

The architecture is based on data quality, traceability, non-diagnostic interpretation and user control.

## Intended Garmin Integration

If Garmin API access is granted, the intended data flow is:

```text
Garmin API
→ OAuth-based user authorization
→ Aura ingestion layer
→ raw data processing
→ metric registry
→ unit conversion
→ data quality validation
→ rejected-data quarantine if needed
→ normalized data store
→ deterministic analytics engine
→ user dashboard
```

## Current Prototype Principles

The current prototype is based on:

- Garmin file import;
- manually entered contextual data;
- normalized metrics;
- local persistence;
- data quality validation;
- rejected-data quarantine;
- deterministic analytics engines.

## Metric Registry

All incoming metrics should be mapped to an internal metric registry before analytics.

This prevents unknown or inconsistent data types from entering the analytics engine.

## Data Quality

Data quality validation is used to evaluate:

- plausibility;
- source reliability;
- freshness;
- unit consistency;
- missing values;
- confidence level.

Low-quality or invalid data may be rejected or placed in quarantine.

## Rejected-Data Quarantine

Rejected data should remain auditable.

The system should store:

- source;
- timestamp;
- metric type;
- value;
- unit;
- rejection reason;
- confidence score.

## Analytics Engine

The deterministic analytics engine may include modules for:

- recovery;
- sleep;
- training load;
- nutrition context;
- mental load;
- readiness;
- risk boundary / safety boundary;
- explainability.

The engine should produce:

- scores;
- confidence levels;
- data used;
- missing data;
- limitations;
- non-diagnostic explanations.

## AI Usage

AI models may be used for summarization, structured extraction or user assistance.

AI should not be the source of final scores or medical conclusions.

## Privacy Architecture

Sensitive manually entered data should be treated separately from Garmin-derived metrics.

Some sensitive categories may remain local-only by default.

## Contact

humanperformance.analytics@gmail.com
