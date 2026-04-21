Unified Alerting & Notification Architecture

Problem Summary
1.) The organization had no mass‑alerting capability for site‑down or widespread outages.
2.) AT&T abruptly disabled email‑to‑SMS, breaking all existing alert delivery from Monitoring systems, SIEM, and RMM Solutions.

Solution Overview
A short description of the architecture:
A multi‑layer alert processing pipeline
Chat‑based routing and pattern matching
API‑driven SMS delivery
Location‑aware and severity‑aware logic
Full auditability through SIEM ingestion

Architecture Diagram:
SEE - Visual Alert Processing Diagram.jpg

Key Features:
Location‑based routing
Severity‑based escalation
Human‑readable audit trail
API‑driven SMS delivery
Multi‑system integration (Nagios, SIEM, Atera)
Resilient to carrier changes
Eliminated dependency on email‑to‑SMS

Contribution:
Identified gaps in alerting and communication
Authored two proposals (mass alerting + SMS replacement)
Designed the full architecture
Built the routing logic and webhook integrations
Implemented the SMS delivery layer
Integrated with SIEM for correlation and retention
Validated the system with on‑call teams and leadership

Impact:
Restored alert delivery after AT&T shutdown
Introduced first‑ever mass alerting capability
Reduced alert delivery failures
Improved response time for outages
Created a repeatable, scalable alerting model
