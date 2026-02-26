# AI-Powered Test Case Executor

## Overview

AI-Powered Test Case Executor is a Python-based automation tool that converts natural language QA test instructions into executable automated browser tests.

The script integrates with the OpenAI GPT API to interpret English test case instructions and automatically execute them on a target web application.

It performs end-to-end validation and generates execution results including pass/fail summaries.

---

## Module

AI-Scripts / Intelligent Test Automation

---

## Problem Statement

Manual execution of written test cases required:

- Reading test case steps
- Opening browser
- Performing actions manually
- Recording pass/fail results

This process was repetitive, time-consuming, and inefficient for regression testing.

---

## Purpose

To automate test execution using natural language input and AI interpretation, reducing manual QA effort.

---

## Technical Stack

- Python
- OpenAI GPT API
- Browser Automation (Selenium / Playwright)
- CLI-based execution
- Automated result reporting

---

## How It Works

1. QA engineer writes test cases in plain English.
2. The script sends the test case instructions to GPT API.
3. GPT interprets steps and generates structured execution logic.
4. The script:
   - Opens the browser
   - Navigates to the project URL
   - Executes all defined test steps
5. The script collects results and displays:
   - Total test cases executed
   - Number of passed cases
   - Number of failed cases

---

## Input Example

Example natural language instruction:

- Open login page
- Enter valid username
- Enter valid password
- Click login
- Verify dashboard loads successfully

---

## Execution Guide

Run from CLI:

```bash
python ai_test_executor.py
