<div align="center">

<img src="images/banner.svg" alt="Vulnerability Management Program banner" width="100%" />

# Vulnerability Management Program

**Standing up a vulnerability management program from zero — policy, stakeholder buy-in, and a full remediation cycle on a simulated enterprise network.**

[![Portfolio](https://img.shields.io/badge/Portfolio-ev--portfolio.com-1E293B?style=flat-square)](https://ev-portfolio.com)
[![Tools](https://img.shields.io/badge/Tools-Tenable%20%7C%20Azure%20%7C%20PowerShell%20%7C%20Bash-334155?style=flat-square)](#tools--technology)

</div>

---

## At a Glance

| | |
|---|---|
| **Role** | Vulnerability Management Analyst (simulated program owner, start to finish) |
| **Scope** | Policy creation → stakeholder buy-in → scanning → prioritization → remediation → maintenance |
| **Result** | **81% reduction** in vulnerabilities (26 → 5) in the first remediation cycle, **100%** of critical findings resolved |
| **Environment** | Windows Server target, provisioned and scanned on Azure |
| **Core tools** | Tenable / Nessus, PowerShell, Bash, Azure Virtual Machines |

> **Inception:** no vulnerability management policy or practices existed.
> **Completion:** a signed-off policy, buy-in from every stakeholder team, and one full remediation cycle delivered end to end.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Tools & Technology](#tools--technology)
- [Program Walkthrough](#program-walkthrough)
  - [1. Draft the Policy](#1-draft-the-policy)
  - [2. Stakeholder Buy-In Meeting](#2-stakeholder-buy-in-meeting)
  - [3. Policy Finalization & Sign-Off](#3-policy-finalization--sign-off)
  - [4. Scan Permission Meeting](#4-scan-permission-meeting)
  - [5. Initial Discovery Scan](#5-initial-discovery-scan)
  - [6. Assessment & Prioritization](#6-assessment--prioritization)
  - [7. Distribute Remediations](#7-distribute-remediations)
  - [8. Post-Scan Review Meeting](#8-post-scan-review-meeting)
  - [9. Change Advisory Board (CAB) Approval](#9-change-advisory-board-cab-approval)
  - [10. Remediation Cycle](#10-remediation-cycle)
- [Results](#results)
- [Ongoing Maintenance](#ongoing-maintenance)

---

## Project Overview

This project simulates running a vulnerability management program inside an organization that has none — from writing the first policy draft through closing out a complete remediation cycle. It's built to mirror the real workflow of a vulnerability management analyst: draft and negotiate policy, get cross-team buy-in, run authenticated scans, triage and prioritize findings, hand off remediation work, and track results through follow-up scans.

---

## Tools & Technology

| Tool | Used for |
|---|---|
| **Tenable / Nessus** | Enterprise vulnerability scanning platform — authenticated scans, reporting |
| **Azure Virtual Machines** | Hosting the Nessus scan engine and the target Windows Server |
| **PowerShell** | Remediation scripting on Windows targets |
| **Bash** | Remediation scripting / automation |

---

## Program Walkthrough

### 1. Draft the Policy
Drafted the initial Vulnerability Management Policy — scope, responsibilities, and remediation timelines — as the starting point for stakeholder conversations.

📎 *Add a link to your draft policy document here.*

### 2. Stakeholder Buy-In Meeting
Presented the draft policy to the server team and stress-tested it against their real capacity to hit remediation timelines. Their feedback reshaped the policy — most notably, extending the critical-vulnerability remediation window from 48 hours to one week.

📸 *[Your screenshot/recording goes here — e.g., meeting thumbnail or notes]*

### 3. Policy Finalization & Sign-Off
Revised the policy based on server team feedback and secured final sign-off from senior leadership, turning it into the governing document for the whole program.

📎 *Add a link to your finalized policy document here.*
📸 *[Your screenshot goes here]*

### 4. Scan Permission Meeting
Negotiated with the server team to start credentialed scanning. Landed on a compromise: scan a single server first, monitor the performance impact, and use just-in-time Active Directory credentials to keep access tightly scoped.

📸 *[Your screenshot/recording goes here]*

### 5. Initial Discovery Scan
Stood up a deliberately insecure Windows Server on Azure to simulate the server team's real environment, introduced known vulnerabilities, then ran an authenticated Nessus scan and exported the results as the baseline for remediation.

📸 *[Your screenshot goes here — Scan 1: Initial Discovery Scan]*

### 6. Assessment & Prioritization
Triaged every finding and built a remediation order based on severity and effort to fix:

1. Windows OS updates (re-enable + apply)
2. Guest account in the local Administrators group
3. Outdated third-party software (Wireshark)
4. SMB signing disabled
5. RDP without Network Level Authentication (NLA)
6. Weak LAN Manager authentication level

### 7. Distribute Remediations
Packaged remediation scripts and scan reports and handed them to the server team, giving them everything needed to fix each finding ahead of a follow-up review.

📎 *Add a link to your remediation email/write-up here.*

### 8. Post-Scan Review Meeting
Walked the server team through the scan results — outdated software, insecure accounts, deprecated protocols — and packaged the remediation plan for submission to the Change Advisory Board (CAB).

📸 *[Your screenshot/recording goes here]*

### 9. Change Advisory Board (CAB) Approval
Presented the plan to disable insecure protocols and cipher suites to the CAB, including a rollback script and a tiered rollout, and got it approved.

📸 *[Your screenshot/recording goes here]*

### 10. Remediation Cycle
Worked through all six findings in priority order, verifying each fix with a follow-up scan:

| Round | Fix | Verified by |
|---|---|---|
| 1 | Re-enabled and applied Windows OS updates | Follow-up scan ✅ |
| 2 | Removed guest account from Administrators group | Follow-up scan ✅ |
| 3 | Removed outdated Wireshark via PowerShell script | Follow-up scan ✅ |
| 4 | Enabled SMB signing to stop man-in-the-middle risk | Follow-up scan ✅ |
| 5 | Enabled Network Level Authentication (NLA) for RDP | Follow-up scan ✅ |
| 6 | Restricted LAN Manager auth to NTLMv2 only | Follow-up scan ✅ |

📸 *[Your screenshots go here — Scans 2 through 7]*

---

## Results

| Metric | Before | After | Change |
|---|---|---|---|
| **Total vulnerabilities** | 26 | 5 | **↓ 81%** |
| **Critical** | — | 0 | **↓ 100%** |
| **High** | 8 | 1 | **↓ 88%** |
| **Medium** | 15 | 3 | **↓ 80%** |

The five remaining findings (SQLite, Microsoft Edge, SSL certificates, ICMP timestamp) were carried into the next remediation cycle. In a real production environment, asset criticality would further shape how those are prioritized.

📸 *[Your final results screenshot/dashboard goes here]*

---

## Ongoing Maintenance

Once the first remediation cycle closed, the program moved into **maintenance mode** — the steady-state process that keeps a vulnerability management program working over time rather than a one-off exercise:

- **Scheduled scans** — recurring scans (weekly/monthly) to catch new vulnerabilities as systems change
- **Patch management** — continuously applying security updates so critical findings don't linger
- **Remediation follow-ups** — triaging and fixing new findings based on risk and impact
- **Policy review** — periodically revisiting the policy against current best practices and org needs
- **Audit & compliance** — internal checks against the policy and any external requirements
- **Stakeholder communication** — keeping remediation teams looped in and coordinated

📎 *Add a link to your finalized policy for the scanning/remediation cadence here.*

---

<div align="center">

Built as a hands-on vulnerability management simulation — see more projects at **[ev-portfolio.com](https://ev-portfolio.com)**

</div>
