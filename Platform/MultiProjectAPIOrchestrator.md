
# Multi-Project API Test & Load Orchestrator

## Overview

Multi-Project API Test & Load Orchestrator is an advanced automation framework designed to perform automated functional API testing and load testing across multiple blockchain explorer projects simultaneously.

The system supports:

- Multi-project API configuration via YAML files  
- Centralized functional test execution  
- Integrated K6 load testing  
- Google Chat alert integration  
- Real-time local dashboard monitoring  
- Structured reporting  

It enables unified API validation, stress testing, and reporting for all explorer projects from a single execution engine.

---

## Problem Statement

Managing API testing across multiple explorer projects is complex and repetitive.

Challenges include:

- Running the same test cases across different projects  
- Performing load testing separately  
- Tracking pass/fail results individually  
- Monitoring real-time execution  
- Sending alerts per project  
- Maintaining centralized visibility  

Manual execution is inefficient and non-scalable.

This platform automates everything in one unified workflow.

---

## Purpose

- Execute common API test cases across multiple projects  
- Perform simultaneous load testing using K6  
- Generate centralized and per-project reports  
- Send structured alerts to project-specific Google Chat groups  
- Provide real-time execution monitoring  

---

## Architecture Overview

The system consists of:

1. YAML Configuration Layer  
   - Each project has its own API configuration file  
   - Project name mapped to its API endpoints  

2. Main Orchestrator Class  
   - Loads all project YAML files  
   - Applies common API test cases  
   - Aggregates results  

3. Functional API Test Engine  
   - Executes predefined general API test cases  
   - Validates response structure, status codes, and data  

4. Load Testing Engine (K6 Integration)  
   - After functional testing  
   - Applies ramp-up load as configured  
   - Runs load test across all project APIs simultaneously  

5. Reporting Engine  
   - Generates detailed execution report  
   - Separates project-wise results  

6. Google Chat Alert System  
   - Sends project-specific alerts  
   - Includes:
     - Total APIs tested  
     - Passed count  
     - Failed count  
     - Skipped count  
     - Failure reasons  
     - Status codes  

7. Local Dashboard  
   - Real-time execution monitoring  
   - Displays:
     - Current project running  
     - API response status  
     - Load execution progress  
     - Pass/Fail updates  

---

## Technical Stack

- Python  
- YAML Configuration  
- Requests Library  
- K6 (Load Testing Engine)  
- Google Chat Webhook Integration  
- Local Dashboard (Flask / Web Interface)  
- Concurrent Execution Handling  

---

## How It Works

1. All explorer projects are defined using YAML files.
2. The main orchestrator loads all project configurations.
3. Common functional API test cases are executed across all projects.
4. Results are recorded project-wise.
5. K6 load testing is triggered using defined ramp-up configuration.
6. Load testing runs simultaneously for all configured projects.
7. Final reports are generated.
8. Alerts are sent to respective Google Chat groups.
9. Execution progress is visible in the local dashboard.

---

## Configuration

Each project requires:

- Project name  
- Base API URL  
- Endpoint definitions  
- Headers (if required)  
- Authentication (if required)  

Load testing configuration includes:

- Ramp-up duration  
- Virtual users  
- Load increment strategy  
- Threshold limits  

Google Chat configuration:

- Webhook URL per project  
- Alert message format  

---

## Execution Guide

python main_orchestrator.py


Ensure:

- Python is installed  
- K6 is installed and accessible  
- YAML files are correctly configured  
- Google Chat webhooks are active  
- Dashboard port is available  

---

## Output

After execution, the system generates:

### Functional Test Summary (Per Project)

- Total APIs Tested  
- Passed  
- Failed  
- Skipped  
- Failure Reasons  
- HTTP Status Codes  

### Load Testing Summary

- Max Load Achieved  
- Failure Threshold  
- Average Response Time  
- Error Percentage  

### Google Chat Alert Example

Each project receives an alert:


Project: Explorer-A

Total APIs: 25
Passed: 22
Failed: 2
Skipped: 1

Failed APIs:

/api/block (500 Internal Server Error)

/api/tx (Timeout)

Overall Status: Partial Failure


### Local Dashboard

During execution, dashboard displays:

- Running project  
- Current API under test  
- Live pass/fail counters  
- Load testing progress  
- Response metrics  

---

## Business Risk Covered

- Prevents unnoticed API regressions  
- Identifies unstable projects before deployment  
- Ensures consistent API behavior across environments  
- Reduces manual multi-project validation effort  
- Provides centralized operational visibility  

---

## ROI

- Saves significant QA and DevOps time  
- Enables parallel project validation  
- Reduces production incident risk  
- Improves infrastructure scalability confidence  
- Provides measurable API reliability metrics  

---

## Stability Level

Current Stability: High

The system performs reliably across multiple projects when properly configured.

Performance depends on:

- Network capacity  
- Server infrastructure  
- K6 configuration  
- System resources  

---

## Security Note

- Do not expose Google Chat webhooks publicly  
- Secure YAML configuration files  
- Use environment variables for secrets  
- Restrict dashboard access to internal network  

---

## Limitations

- Load testing depends on system machine capacity  
- Dashboard requires local server availability  
- Parallel testing increases resource usage  
- Requires proper YAML configuration structure  

---

## Future Enhancements

- Distributed load testing cluster  
- Historical trend analytics  
- Database-backed reporting  
- Role-based dashboard access  
- Slack / Email alert integration  
- CI/CD pipeline integration  

---

## Maintained By

Sahil  
Automation Architect & Infrastructure Engineer

Run from CLI:
