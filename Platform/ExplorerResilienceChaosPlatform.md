# Explorer Resilience & Chaos Engineering Platform

## Overview

Explorer Resilience & Chaos Engineering Platform is an advanced infrastructure validation system designed to test the stability, scalability, and recovery behavior of a blockchain explorer ecosystem.

The platform integrates:

- Full API automation  
- RPC validation  
- K6 load testing  
- Real-time dashboard monitoring  
- Google Chat alerting  
- Chaos Monkey infrastructure testing  

It intentionally disrupts infrastructure components such as RPC nodes, instances, ports, and network access to evaluate system resilience and recovery mechanisms.

---

## Problem Statement

Blockchain explorer systems rely on:

- Multiple RPC nodes  
- Distributed instances  
- Network ports  
- Regional infrastructure  
- DevOps-managed environments  

Failures such as:

- RPC shutdown  
- Instance crash  
- Port closure  
- Network disruption  
- Regional node outage  

can cause service degradation or downtime.

Traditional testing does not simulate real infrastructure failures.

This platform validates system behavior under controlled infrastructure chaos.

---

## Purpose

- Validate API and RPC stability  
- Apply load using K6  
- Simulate infrastructure failures  
- Test failover mechanisms  
- Verify auto-recovery and syncing  
- Monitor resilience in real time  
- Send structured alerts  

---

## Architecture Overview

The system consists of:

1. API Automation Layer  
   - Executes all explorer APIs  
   - Validates responses  
   - Records pass/fail metrics  

2. RPC Testing Layer  
   - Validates RPC health  
   - Checks block syncing  
   - Ensures response correctness  

3. Load Testing Engine (K6)  
   - Applies ramp-up load  
   - Measures stress tolerance  

4. Chaos Monkey Module  
   - Uses DevOps-provided configuration  
   - Contains:
     - Node IP addresses  
     - Region details  
     - SSH keys  
     - Instance identifiers  
   - Randomly shuts down:
     - RPC services  
     - Instances  
     - Specific ports  
     - Network access  
   - Observes system behavior  

5. Recovery & Retest Engine  
   - Restarts affected services  
   - Re-validates API behavior  
   - Checks RPC syncing status  
   - Confirms system stability post-recovery  

6. Dashboard System  
   - Live execution tracking  
   - Displays:
     - Active chaos events  
     - API failures  
     - RPC downtime  
     - Load metrics  
     - Recovery status  

7. Alerting Engine  
   - Sends structured alerts  
   - Includes:
     - Failure reason  
     - Affected node  
     - Recovery confirmation  
     - Sync status  

---

## Technical Stack

- Python  
- Requests Library  
- SSH Automation  
- YAML Configuration  
- K6 Load Testing  
- Google Chat Webhooks  
- Real-Time Dashboard (Flask / Web UI)  
- Chaos Monkey Logic  

---

## Functional Flow

### Phase 1 – Normal Execution

1. Execute all Explorer APIs  
2. Validate RPC endpoints  
3. Apply K6 load testing  
4. Monitor responses  

---

### Phase 2 – Chaos Injection

1. Random RPC shutdown  
2. Instance termination  
3. Port blocking  
4. Network disruption  

System monitors:

- API failure behavior  
- Timeout handling  
- Error responses  
- Failover behavior  

---

### Phase 3 – Recovery Validation

1. Restart RPC / Instance  
2. Re-test all APIs  
3. Validate RPC syncing  
4. Confirm block height consistency  
5. Ensure load stability  
6. Generate final recovery report  

---

## Execution Guide

python explorer_chaos_platform.pyRun Full Platform:


Ensure:

- DevOps configuration file is complete  
- SSH keys are valid  
- K6 is installed  
- Explorer API and RPC endpoints are configured  
- Dashboard port is available  

---

## Output

### Functional Test Report

- Total APIs Tested  
- Passed  
- Failed  
- RPC Status  

---

### Chaos Event Report

Example:

Chaos Event: RPC Node Shutdown
Affected Node: 10.0.1.24 (Region: Asia)

API Failures Detected: 5
Timeouts: 3
Error Codes: 500, 503

Recovery Initiated...
RPC Restarted
Sync Status: Verified
Post-Recovery API Status: Stable


---

### Load Test Metrics

- Virtual Users  
- Error Rate  
- Average Response Time  
- Stability Score  

---

### Alert Structure

Each project group receives:

- API Summary  
- Chaos Event Triggered  
- Affected Infrastructure  
- Recovery Status  
- Sync Validation  
- Final Stability Status  

Alerts are sent separately for:

- Normal test run  
- Chaos event  
- Post-recovery validation  

---

## Dashboard Capabilities

During execution:

- Active Chaos Status  
- Running API  
- RPC Health Indicator  
- Instance State  
- Load Metrics  
- Recovery Progress  

---

## Business Risk Covered

- Prevents catastrophic production outages  
- Validates failover reliability  
- Detects weak infrastructure points  
- Measures recovery time  
- Ensures blockchain syncing integrity  
- Strengthens DevOps confidence  

---

## ROI

- Reduces downtime cost  
- Improves system reliability  
- Enables infrastructure stress validation  
- Provides measurable resilience metrics  
- Enhances release confidence  

---

## Stability Level

Current Stability: Advanced

The platform is suitable for:

- Staging environments  
- Pre-production testing  
- Controlled production validation (with approval)  

---

## Security Note

- Protect SSH keys securely  
- Restrict chaos execution to authorized environments  
- Do not expose infrastructure configuration files  
- Run chaos tests only with DevOps approval  

---

## Limitations

- Requires DevOps coordination  
- Resource intensive  
- Chaos testing may impact shared infrastructure  
- Not recommended for uncontrolled production use  

---

## Future Enhancements

- Automated rollback verification  
- Multi-region failover testing  
- Container-level chaos (Kubernetes integration)  
- Real-time resilience scoring  
- Historical chaos analytics  

---

## Maintained By

Sahil  
Automation Architect | Chaos Engineer | Infrastructure Resilience Specialist

