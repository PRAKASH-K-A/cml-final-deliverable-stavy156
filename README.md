[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/aQj7XJJr)
# Observability Module – Telemetry Service

## Author
**Stavya Pandey**  
Roll No: 230958086  
Group: 3  

---

## Overview
This module implements **observability (telemetry)** for a simulated trading system.

It provides real-time insights into:
- Trade activity
- Market data updates
- Option pricing updates
- System health metrics

The telemetry system aggregates data from multiple services and logs it periodically.

---

## Objective
The goal of this module is to:
- Monitor system performance
- Track event frequency
- Provide runtime visibility
- Assist debugging and validation

---

## Tech Stack
- Java
- Spring Boot
- Spring Scheduler (`@Scheduled`)
- SLF4J Logging

---

## System Components

### 🔹 TradeAuditService
- Stores trades in database
- Provides:
  - Total trade count
  - Last trade timestamp

---

### 🔹 MarketDataPoller
- Simulates market updates
- Tracks:
  - Update count
  - Last update time

---

### 🔹 PricingService
- Computes option pricing
- Tracks:
  - Pricing update count
  - Last pricing update time

---

### 🔹 TelemetryService (This Module)
- Aggregates all metrics
- Logs telemetry every 10 seconds

---

## Data Flow and Sample Output
Telemetry: totalTrades=150
lastTradeTime=2026-03-02T16:43:10Z
marketUpdatesCount=45
optionUpdatesCount=42
lastMarketUpdateTime=2026-03-02T16:43:08Z
lastOptionUpdateTime=2026-03-02T16:43:09Z
