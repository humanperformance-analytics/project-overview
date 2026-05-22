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
