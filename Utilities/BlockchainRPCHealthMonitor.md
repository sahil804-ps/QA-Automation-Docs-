# Blockchain RPC Health Monitor

## Overview

Blockchain RPC Health Monitor is a Python-based continuous monitoring tool designed to track the operational health of multiple blockchain projects.

It verifies:

- RPC endpoint availability  
- Block synchronization progress  
- API responsiveness  
- P2P transaction functionality  

The script runs continuously via CLI and triggers an audible alert (beep sound) if any monitored service becomes unavailable.

---

## Module

Utilities / Blockchain Infrastructure Monitoring

---

## Problem Statement

As a QA engineer, daily manual verification was required for multiple blockchain projects to ensure:

- RPC endpoints were responding
- Blocks were syncing correctly
- APIs were functional
- Transactions were being processed

This repetitive process consumed significant time and risked delayed detection of infrastructure failures.

---

## Purpose

To automate real-time monitoring of blockchain infrastructure and instantly alert when any service disruption occurs.

---

## Technical Stack

- Python
- CLI Execution
- RPC API Calls
- Block Height Validation APIs
- Local Audible Alert System

---

## Projects Monitored

- 10+ blockchain projects
- Multiple RPC endpoints
- Block synchronization APIs
- Transaction broadcast validation

---

## Technical Flow

1. Load predefined RPC and API endpoints.
2. Send health-check requests.
3. Validate:
   - RPC response status
   - Latest block height progression
   - API responsiveness
4. If a failure is detected:
   - Retry up to 3 times
   - Wait 2 minutes between each retry
5. If all 3 retries fail:
   - Trigger audible beep alert
   - Log affected project name
6. Continue monitoring loop.

---

## Retry Mechanism

The script includes built-in retry handling to prevent false failure alerts.

- Maximum Retries: 3  
- Retry Interval: 2 minutes  
- Alert Trigger Condition: After all retries fail  

This ensures temporary network fluctuations do not generate false alarms.

---

## Authentication

No login or authentication is required.  
All monitored endpoints are public RPC or API endpoints.

---

## Execution Guide

Run from CLI:

```bash
python rpc_monitor.py
