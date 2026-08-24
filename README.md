# Pricing & Revenue Analysis

### Business Intelligence · SQL · Data Analysis · Revenue Optimization

## Overview

Analyzed historical and current procedure rates across 30+ insurance providers to identify pricing differences, prioritize high-impact opportunities, and evaluate potential revenue impact from rate negotiations.

The analysis combined complex insurer-specific pricing structures with business context to determine the appropriate rate for each procedure and quantify the financial impact of potential changes over time.

> **Note:** This project is based on professional experience. Company names, proprietary data, actual insurance rates, and internal systems are not included. The examples and datasets in this repository are synthetic and created for demonstration purposes.

---

## Business Problem

Procedure rates varied significantly across insurance providers, and each insurer maintained its own pricing structure.

The analysis needed to account for:

- Historical and current procedure rates
- Insurer-specific geographic regions
- Specialty-specific pricing
- Procedure-specific payment structures
- Effective dates
- Procedures with multiple payment components
- Differences in how and when procedure rates were recognized

Because of these differences, comparing the listed rate alone was not always sufficient to determine the true total rate for a procedure.

The goal was to create a reliable view of procedure-level pricing, identify the highest-value opportunities, and quantify the potential revenue impact of negotiated rate changes.

---

## Data & Pricing Logic

### Insurer-Specific Rates

Each insurance provider maintained its own pricing structure and regional definitions.

A single procedure could have different rates based on:

**Insurance Provider → Region → Specialty → Procedure → Effective Date**

Regional definitions were not standardized across insurers, so the analysis used each insurer's own geographic structure when determining the applicable rate.

### Specialty

Rates could also vary based on provider specialty.

For example:

```text
Procedure X
├── General Dentistry → Rate A
└── Pediatric Dentistry → Rate B
