# Unified Alerting & Notification Architecture
Author: Alex

Status: Implemented (Sanitized)

## Overview
This project delivers a unified, resilient alerting and notification architecture that replaces legacy email-to-SMS delivery and introduces the organization’s first mass-alerting capability. The system integrates ITIM (monitoring), SIEM (correlation and audit), and an Endpoint Management Platform into a centralized routing and delivery pipeline.

The architecture is designed for:
- High-severity incident response  
- Site-wide and company-wide broadcast alerts  
- Reliable SMS delivery via API  
- Human-readable audit trails  
- Multi-system integration  
- Location-aware and severity-aware routing  

---

## Problem Summary

### 1. No Mass Alerting Capability
Before this project, the organization had no mechanism to notify all employees or specific locations during widespread outages. Communication was manual, inconsistent, and slow.

### 2. AT&T Disabled Email-to-SMS
AT&T’s shutdown of email-to-text broke all SMS alerts from:
- ITIM (monitoring)
- SIEM (security events)
- Endpoint Management Platform (agent health)

This resulted in silent failures and loss of operational visibility.

---

## Solution Summary
This architecture introduces a multi-layer alerting pipeline:

1. **Monitoring Layer**  
   ITIM, SIEM, and Endpoint Management Platform generate structured webhook events.

2. **Routing Layer (Chat-Based Message Bus)**  
   Alerts are posted into a dedicated ingestion channel, parsed using pattern-based logic, and routed based on severity and location.

3. **Notification Delivery Layer**  
   API-driven SMS delivery replaces email-to-SMS and supports mass broadcast.

4. **Recipient Layer**  
   On-call teams, NOC/SOC, engineering, and leadership receive alerts based on escalation rules.

5. **Logging & Intelligence Layer**  
   SIEM ingests all events, routing decisions, and delivery logs for correlation and auditability.

---

## Architecture Diagram
See `/diagrams/alerting-architecture.png`  
Mermaid source is included in `/diagrams/alerting-architecture.mmd`.

---

## Key Features
- API-based SMS delivery (carrier-independent)  
- Mass alerting for site-wide and company-wide events  
- Pattern-based routing logic  
- Human-readable audit trail via chat ingestion  
- SIEM correlation and retention  
- Multi-system integration (monitoring, endpoint, security)  
- Escalation chains with time-based logic  

---

## Your Contribution
- Authored two proposals (mass alerting + SMS replacement)  
- Designed the full architecture from first principles  
- Implemented routing logic and webhook ingestion  
- Built SMS delivery integration  
- Integrated SIEM logging for audit and correlation  
- Validated the system with on-call teams and leadership  
- Delivered the organization’s first mass-alerting capability  

---

## Repository Structure

