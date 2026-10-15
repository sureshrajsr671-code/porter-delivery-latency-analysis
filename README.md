# Porter Delivery Time Optimization and Latency Analysis

Diagnosing Operational Latency, Supply-Demand Imbalances, and Actionable Interventions to Reclaim CSAT.

---

## Executive Diagnostics and Overview
An empirical investigation across 175,000+ delivery transactions across 6 metro markets to diagnose operational latency and reverse customer dissatisfaction.

### Key Performance Metrics
- Target Benchmark Delivery Window: 32.0 minutes
- Average Actual Delivery Time: 48.6 minutes
- Customer Expectation Gap: +16.6 minutes deficit
- SLA Breach Rate: Over 38.4% of deliveries experienced SLA breaches exceeding 15 minutes, directly driving app rating declines and order cancellations.

---

## Dataset and Analytics Framework
- Order Records Analyzed: 175,777 unified transaction logs across 6 metro markets.
- Target Variable Analysis: Quantified end-to-end duration from order placement (created_at) to completed handover (actual_delivery_time).
- Fleet Capacity Variables: Evaluated on-shift delivery partners, busy couriers ratio, and live order backlogs.

---

## Operational Bottlenecks and Root Drivers

### 1. Kitchen Preparation Delays (54% of Total Variance)
- Restaurant turnaround accounts for 54% of total delivery latency variance.
- Complex cuisines (Italian, Indian, artisanal pizzas) and large orders (>4 items) average 26.8 minutes of prep time before courier pickup.

### 2. Fleet Supply Starvation and Peak Congestion
- During lunch (12:00 PM - 2:00 PM) and dinner peaks (7:00 PM - 10:00 PM), the ratio of busy dashers exceeds 88%.
- Couriers assigned mid-delivery experience 12-18 minutes of pre-dispatch queue time.
- When outstanding orders exceed active available drivers by 2.5x, dispatch lag escalates from 4 minutes to 19 minutes.

### 3. Protocol Friction and Courier Burnout
- Orders routed through manual call-in protocols (Code 3 and 4) suffer 13.4 minutes longer turnaround compared to direct POS integrations.
- Uncompensated counter wait times reduce courier peak hourly earnings by 28%, causing driver log-offs during dinner peaks.

---

## Market and Channel Risk Matrix

| Market and Ordering Channel | Order Share | Avg Delivery Time | Dasher Deficit Ratio | SLA Risk Level |
| :--- | :--- | :--- | :--- | :--- |
| Market 2 - Fast Food and Pizza | 28.4% | 53.2 mins | 1.84 (Severe Backlog) | Critical |
| Market 4 - Casual Dine-in | 18.6% | 49.8 mins | 1.62 (High Load) | Critical |
| Protocol 3 - Call-in Dispatch | 12.2% | 51.6 mins | 1.45 (Manual Queue) | High |
| Market 1 - Mixed Retail | 24.1% | 45.1 mins | 1.18 (Moderate) | High |
| Protocol 1 - Direct POS | 36.7% | 38.2 mins | 0.92 (Balanced) | Moderate |
| Market 3 - Stable Core | Baseline | 41.4 mins | Balanced | Stable |

---

## Strategic Turnaround Roadmap

- Q1 - Dynamic Machine Learning ETA: Deploy multi-feature neural regression models to predict dynamic, real-world ETAs using live order queues and traffic data.
- Q2 - Merchant SLAs and POS Integration: Mandate kitchen tablet confirmations, replace manual call-in protocols with direct POS connections, and penalize merchant wait times exceeding 12 minutes.
- Q3 - Supply Re-Balancing: Proactively relocate fleets to high-order clusters 30 minutes ahead of peak demand using geofenced surge incentives.
- Q4 - Staged Just-In-Time Dispatch: Synchronize courier dispatch to actual kitchen packing completion rather than initial order receipt, eliminating idle courier wait times.

---

## Repository Structure
```text
├── data/
│   └── porter_delivery_dataset.csv
├── working_files/
│   └── Porter_Delivery_Latency_Working_File.xlsx
├── screenshots/
│   └── porter_delivery_dashboard_v2.png
├── presentation/
│   └── Porter Delivery Latency Analysis.pptx
└── README.md
