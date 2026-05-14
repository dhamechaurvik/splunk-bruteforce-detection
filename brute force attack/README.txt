# 🔐 Splunk Brute Force Detection System

## 📌 Project Overview
A cybersecurity project to detect brute force login attacks using Splunk SIEM.
Simulates failed login attempts, ingests logs, and uses SPL queries to detect
and alert on suspicious activity.

## 🛠️ Tools Used
- Splunk Enterprise (Free Trial)
- Windows 10/11
- SPL (Search Processing Language)

## 🎯 MITRE ATT&CK Mapping
- Technique: T1110 — Brute Force
- Tactic: Credential Access

## 📁 Project Structure
splunk-bruteforce-detection/
├── logs/auth_login.log        # Simulated brute force log data
├── spl_queries/               # All SPL detection queries
├── screenshots/               # Splunk search and dashboard screenshots
└── README.md

## 🔍 SPL Queries
| File | Purpose |
|------|---------|
| 01_verify_data.spl | Verify data ingestion |
| 02_failed_logins.spl | List all failed logins |
| 03_brute_force_count.spl | Count failures per IP |
| 04_compromised_accounts.spl | Detect successful breach after brute force |
| 05_alert_query.spl | Real-time alert trigger query |

## 🚨 Alert Configuration
- Trigger: 4+ failed logins from same IP
- Schedule: Every 5 minutes
- Severity: High
- Action: Add to Triggered Alerts

## 📊 Dashboard Panels
- Failed Login Events Table
- Top Attacking IPs Chart
- Failed Logins Over Time
- Compromised Accounts Table

## 📸 Screenshots
See screenshots/ folder for full project walkthrough.