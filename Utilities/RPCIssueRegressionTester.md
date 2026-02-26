
# RPC Issue Regression Tester

## Overview

RPC Issue Regression Tester is a Python-based validation tool designed to test a blockchain RPC endpoint against previously identified real-world RPC issues.

The script maintains a collection of historical RPC failure scenarios and automatically validates any new RPC endpoint against those cases.

It provides a structured report showing pass/fail results and overall RPC health status.

---

## Problem Statement

Blockchain RPC endpoints often fail under specific edge cases such as:

- Invalid responses  
- Timeout issues  
- Block height inconsistencies  
- Rate limits  
- Malformed JSON-RPC responses  

When switching RPC providers or updating infrastructure, previously resolved issues may reappear.

Manual re-validation is inefficient and error-prone.

This tool automates regression testing for RPC stability.

---

## Purpose

- Validate RPC against historical issue cases  
- Detect recurring infrastructure bugs  
- Measure RPC reliability before production use  
- Provide structured health evaluation  

---

## Technical Stack

- Python  
- Requests Library  
- JSON-RPC  
- Environment Configuration (.env)  
- Automated Test Case Execution  

---

## How It Works

1. A collection of known RPC issue test cases is maintained inside the script.
2. User updates:
   - RPC endpoint URL  
   - Environment configuration  
3. The script executes all stored issue scenarios against the provided RPC.
4. Each test validates:
   - Response structure  
   - Response time  
   - Data correctness  
   - Error handling  
5. The script generates a pass/fail summary.
6. Overall RPC health is calculated based on success rate.

---

## Configuration

Before running the script:

- Update the RPC URL
- Configure environment variables if required
- Ensure internet connectivity

The script dynamically adapts to the provided RPC endpoint.

---

## Execution Guide


python rpc_issue_regression.py


Make sure:

- Python is installed  
- Dependencies are installed  
- RPC endpoint is correctly configured  

---

## Output

After execution, the script provides a structured summary in the terminal.

It displays:

- Total test cases executed  
- Number of passed cases  
- Number of failed cases  
- Failure reason per test case  
- Overall RPC Health Score  

Example:

RPC Endpoint: https://example-rpc.com

Total Test Cases: 15
Passed: 13
Failed: 2

Health Score: 86%
Status: Stable


If failures occur, detailed error information is displayed for debugging.

---

## Business Risk Covered

- Prevents deploying unstable RPC endpoints  
- Detects historical issue recurrence  
- Reduces production outages  
- Improves blockchain infrastructure reliability  

---

## ROI

- Saves infrastructure debugging time  
- Reduces risk of RPC migration failures  
- Improves deployment confidence  
- Provides measurable RPC quality score  

---

## Stability Level

Current Stability: High

The script performs consistently when validating standard JSON-RPC endpoints.

Performance depends on network stability and RPC responsiveness.

---

## Security Note

- Do not expose private RPC endpoints publicly  
- Avoid committing sensitive environment variables  
- Store configuration securely  
- Ensure access control for production RPCs  

---

## Limitations

- Limited to predefined historical issue cases  
- No automatic test case generation  
- Terminal-based reporting only  
- No real-time alerting  

---

## Future Enhancements

- Dynamic issue case learning  
- Automatic log storage  
- Dashboard-based health visualization  
- Multi-RPC comparison testing  
- CI/CD integration  

---

## Maintained By

Sahil  
Blockchain Infrastructure & Automation Developer

Run from CLI:
