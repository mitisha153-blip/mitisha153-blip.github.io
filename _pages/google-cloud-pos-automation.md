---
layout: single
title: "Google Cloud POS Data Automation"
permalink: /projects/google-cloud-pos-automation/
author_profile: false
classes: wide
---

<style>
.cloud-metrics {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 14px;
  margin: 24px 0;
}
.cloud-metric {
  background: #f1f6f8;
  border: 1px solid #dce5ec;
  border-radius: 12px;
  padding: 18px 12px;
  text-align: center;
}
.cloud-metric strong {
  display: block;
  color: #17365d;
  font-size: 1.65rem;
}
.cloud-metric span {
  display: block;
  color: #526477;
  font-size: 0.83rem;
  margin-top: 6px;
}
.cloud-pipeline {
  display: flex;
  align-items: stretch;
  gap: 8px;
  margin: 24px 0;
}
.cloud-step {
  flex: 1;
  min-width: 0;
  background: #f1f6f8;
  border: 1px solid #dce5ec;
  border-radius: 10px;
  padding: 16px 10px;
  text-align: center;
}
.cloud-step strong {
  display: block;
  color: #17365d;
  font-size: 0.9rem;
}
.cloud-step span {
  display: block;
  color: #526477;
  font-size: 0.76rem;
  margin-top: 7px;
}
.cloud-arrow {
  align-self: center;
  color: #087f8c;
  font-weight: 700;
  font-size: 1.3rem;
}
@media (max-width: 750px) {
  .cloud-pipeline {
    flex-direction: column;
  }
  .cloud-arrow {
    transform: rotate(90deg);
  }
  .cloud-metrics {
    grid-template-columns: 1fr;
  }
}
</style>

<p style="color:#64748b;font-size:1.05rem;">
  Data Engineering | Cloud Automation | Google Cloud
</p>

## Business Problem

Point-of-sale (POS) systems generate transaction
files that need to be processed before they can
support business reporting and analytics.

Manually loading files into a data warehouse can
be time-consuming and prone to errors.

The goal of this project was to develop an
automated workflow that could:

- Detect newly uploaded POS files.
- Load incoming data into BigQuery.
- Refresh cleaned analytical tables.
- Identify missing files for follow-up.

## Technical Architecture

The solution combined Google Cloud services
to automate data ingestion and processing.

<div class="cloud-pipeline" role="img"
aria-label="Pipeline showing Cloud Storage, Eventarc, Cloud Run, BigQuery raw tables, and scheduled clean table refresh.">

  <div class="cloud-step">
    <strong>Cloud Storage</strong>
    <span>POS CSV files uploaded</span>
  </div>

  <div class="cloud-arrow">&rarr;</div>

  <div class="cloud-step">
    <strong>Eventarc</strong>
    <span>Detects file events</span>
  </div>

  <div class="cloud-arrow">&rarr;</div>

  <div class="cloud-step">
    <strong>Cloud Run</strong>
    <span>Executes loading logic</span>
  </div>

  <div class="cloud-arrow">&rarr;</div>

  <div class="cloud-step">
    <strong>BigQuery</strong>
    <span>Stores raw POS data</span>
  </div>

  <div class="cloud-arrow">&rarr;</div>

  <div class="cloud-step">
    <strong>Scheduled SQL</strong>
    <span>Refreshes clean tables</span>
  </div>

</div>

*Simplified architecture of the automated POS
data processing workflow.*

## Implementation

### 1. Event-Driven File Ingestion

Configured an Eventarc trigger to respond
to new files arriving in Cloud Storage.

The trigger invokes a Cloud Run service
responsible for processing incoming POS files.

### 2. BigQuery Data Loading

Used BigQuery to store transaction data from
three POS sources:

- Cornfield
- JoePOS
- Wabash

The workflow supported ingestion of incoming
order files and associated data.

### 3. Automated Data Refresh

Configured a scheduled BigQuery query to
refresh cleaned tables for downstream analysis.

This reduced the need to manually rerun
data transformation queries after new files
were loaded.

### 4. Missing File Monitoring

Checked expected files against available
source files to identify missing inputs.

This provided a way to investigate incomplete
data deliveries before relying on downstream
reporting.

## Results

The project reached the following recorded
order-data totals:

<div class="cloud-metrics">
  <div class="cloud-metric">
    <strong>128,706</strong>
    <span>Cornfield order rows</span>
  </div>
  <div class="cloud-metric">
    <strong>176,383</strong>
    <span>JoePOS order rows</span>
  </div>
  <div class="cloud-metric">
    <strong>89,408</strong>
    <span>Wabash order rows</span>
  </div>
</div>

### Data Loading Summary

| POS Source | Order Rows | Files Recorded |
|---|---:|---:|
| Cornfield | 128,706 | 30 |
| JoePOS | 176,383 | 30 |
| Wabash | 89,408 | 30 |
| **Total** | **394,497** | **90** |

*These figures reflect recorded project load
totals, not a production-scale deployment.*

## Challenges & Lessons Learned

**Data completeness:** An automated pipeline
still requires checks to ensure expected
files have arrived.

**Operational reliability:** Monitoring logs
and investigating load failures are important
parts of maintaining a data workflow.

**Automation:** Event-driven services and
scheduled queries can reduce repetitive
manual processing.

**Analytics readiness:** Reliable data
ingestion and cleaning provide the foundation
for meaningful reporting and analysis.

## Tools & Technologies

- Google Cloud Storage
- Eventarc
- Cloud Run
- BigQuery
- SQL
- Cloud Logging

## Key Takeaway

This project strengthened my understanding
of how cloud services can work together to
move data from operational systems into
analytical tables.

It also demonstrated that successful
data engineering involves more than loading
data: completeness checks, monitoring, and
reliable refresh processes are essential.

---

[Back to All Projects](/projects/)
