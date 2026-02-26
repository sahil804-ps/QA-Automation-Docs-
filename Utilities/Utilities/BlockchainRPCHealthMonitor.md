
# Blockchain RPC Health Monitor

## Overview

A Python-based continuous monitoring script designed to track the health status of multiple blockchain projects.  
The script validates RPC availability, block synchronization status, and P2P transaction functionality in real time.

It runs continuously via CLI and provides an audible alert (beep sound) when any monitored service becomes unavailable or unstable.

---

## Module

Utilities / Blockchain Monitoring

---

## Problem Statement

As a QA engineer, daily manual verification was required for:

- RPC endpoint availability
- Block syncing status
- P2P transaction flow
- API responsiveness

This process had to be repeated every morning across multiple projects, consuming significant time and risking delayed detection of outages.

---

## Purpose

To automate continuous monitoring of blockchain infrastructure and provide instant alerts in case of service disruption.

---

## Technical Stack

- Python
- CLI Execution
- RPC API Calls
- Block Height Validation API
- System Beep Alert Mechanism

---

## Projects Monitored

- 10+ blockchain projects
- Multiple RPC endpoints
- Block synchronization APIs
- Transaction broadcast validation

---

## Technical Flow

1. Load predefined RPC and API endpoints.
2. Send periodic health-check requests.
3. Validate:
   - RPC response status
   - Latest block height increment
   - API responsiveness
4. If validation fails:
   - Trigger audible beep alert
   - Identify affected project
5. Continue monitoring in loop (24/7 execution).

---

## Test Coverage

- RPC availability check
- Block sync progression check
- API status validation
- Failure detection logic
- Continuous runtime monitoring

---

## Execution Guide

Run from CLI:
