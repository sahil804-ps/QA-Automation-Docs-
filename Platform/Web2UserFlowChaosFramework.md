
# Web2 User Flow Automation & Chaos Engineering Framework

## Overview

Web2 User Flow Automation & Chaos Engineering Framework is a Python-based end-to-end automation system designed to simulate real user journeys, validate role-based access control, monitor API behavior, and test system resilience under controlled failure conditions.

The framework executes complete user workflows such as:

- User Signup  
- Login  
- Role-Based Access Validation  
- Purchase Flow  
- Dashboard Interaction  
- Logout  

In addition, it includes a Chaos Engineering module that intentionally injects latency and controlled failures to evaluate system stability and response behavior.

The system generates structured reports, sends real-time alerts, and provides live execution monitoring via a dashboard.

---

## Problem Statement

Modern Web2 applications with:

- Role-based access control  
- Purchase systems  
- Dashboard workflows  

require validation beyond isolated API testing.

Risks include:

- Broken user flows  
- Role permission leaks  
- Checkout failures  
- Performance degradation  
- Unhandled API latency  

Traditional API testing does not simulate real user behavior or system stress scenarios.

This framework addresses both functional correctness and resilience validation.

---

## Purpose

- Automate complete real-world user journeys  
- Validate role-based permissions  
- Monitor API success/failure in real time  
- Simulate failure conditions using Chaos Engineering  
- Measure system resilience under latency injection  
- Provide project-specific alerts and reports  

---

## Architecture Overview

The system consists of:

1. User Flow Automation Engine  
   - Executes complete user lifecycle  
   - Simulates real user scope  
   - Validates responses and transitions  

2. Role-Based Access Validator  
   - Ensures correct permission mapping  
   - Validates restricted endpoints  

3. Dashboard Monitoring System  
   - Real-time execution visibility  
   - Live pass/fail tracking  
   - API response metrics  

4. Alerting Engine  
   - Sends structured alerts to project-specific groups  
   - Includes pass/fail/skip metrics  
   - Displays failure reasons  

5. Chaos Engineering Module  
   - Injects artificial latency  
   - Simulates degraded API responses  
   - Captures system behavior under stress  
   - Generates separate resilience report  

---

## Technical Stack

- Python  
- Requests Library  
- Concurrent Execution Handling  
- Real-Time Dashboard (Flask / Web Interface)  
- Google Chat Webhook Alerts  
- Chaos Simulation Logic (Latency Injection)  

---

## Functional Flow

### Normal Execution Mode

1. Simulate user signup
2. Perform login
3. Validate authentication token
4. Execute role-based actions
5. Perform purchase flow
6. Access dashboard
7. Logout
8. Generate execution report
9. Send project-specific alert

---

### Chaos Mode Execution

When Chaos file is executed:

1. Same user journey flow runs
2. Artificial latency is introduced into APIs
3. Controlled delays simulate degraded performance
4. Response behavior is captured
5. Screenshots (if UI involved) are recorded
6. Failure tolerance is evaluated
7. Separate Chaos Report is generated
8. Dedicated alert is sent with resilience results

---

## Execution Guide
python user_flow_runner.py


Run Chaos Mode:


python chaos_runner.py


Ensure:

- Python is installed  
- Required dependencies are installed  
- Project API endpoints are configured  
- Dashboard port is available  
- Alert webhooks are active  

---

## Output

### Functional Execution Report

- Total APIs executed  
- Passed  
- Failed  
- Skipped  
- User flow status  
- Role validation result  

Example:

Project: Web2 Application

Total Steps: 18
Passed: 16
Failed: 2
Skipped: 0

Overall Flow Status: Partial Failure


---

### Chaos Engineering Report

- Latency injected (ms)  
- Response degradation percentage  
- Timeout occurrences  
- API failure behavior  
- Recovery status  

Example:

Chaos Mode Enabled
Injected Latency: 500ms

Timeouts: 2
Delayed Responses: 5
Failed Transactions: 1

System Resilience Status: Moderate


---

## Dashboard Capabilities

During execution:

- Current flow step  
- Live API response times  
- Pass/Fail counters  
- Chaos injection indicator  
- Error logs  

---

## Google Chat Alert Structure

Project-specific alerts include:

- Total steps executed  
- Passed/Failed/Skipped  
- Failure reasons  
- HTTP status codes  
- Chaos results (if enabled)  

Alerts are separated for:

- Normal execution  
- Chaos execution  

---

## Business Risk Covered

- Prevents broken production user flows  
- Detects permission leaks  
- Identifies checkout failures  
- Measures system tolerance to latency  
- Reduces production outages  
- Improves release confidence  

---

## ROI

- Eliminates manual user flow testing  
- Reduces post-deployment bug discovery  
- Improves system reliability metrics  
- Provides resilience benchmarking  
- Enhances infrastructure stability  

---

## Stability Level

Current Stability: High

The framework performs reliably for role-based Web2 applications.

Chaos mode results depend on:

- Infrastructure capacity  
- Backend timeout handling  
- Error management logic  

---

## Security Note

- Do not expose webhook URLs  
- Secure authentication tokens  
- Avoid running chaos tests on live production without approval  
- Store configuration securely  

---

## Limitations

- Chaos testing limited to latency simulation  
- Resource intensive for large workflows  
- Requires stable environment configuration  
- Dashboard is local unless deployed  

---

## Future Enhancements

- Packet loss simulation  
- Auto-recovery detection scoring  
- Distributed chaos injection  
- Persistent log storage  
- Historical resilience trend analysis  
- CI/CD integration  

---

## Maintained By

Sahil  
Automation Architect | QA Infrastructure | Resilience Engineer

Run Normal Mode:
