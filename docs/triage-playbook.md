# Security Event Triage Playbook

A repeatable process for reviewing an alert or suspicious event in a lab environment.

## 1. Identify the alert

Capture the basic facts:

- event type
- host/source
- user or process involved
- timestamp
- severity or rule context

## 2. Validate the data source

Before investigating the event itself, make sure the telemetry is trustworthy:

- endpoint/source is online
- collection path is functioning
- timestamps are aligned
- expected event source is enabled

## 3. Establish context

Ask:

- Is this activity expected on the host?
- What happened immediately before and after it?
- Is the user/process/service known?
- Is there related network activity?

## 4. Correlate network evidence

Use packet or firewall context where available to determine whether communication was attempted, allowed, blocked, or otherwise relevant to the event.

## 5. Separate fact from inference

Document what is directly observed separately from what is suspected. An alert is evidence to review, not proof by itself.

## 6. Escalate or close

In a real operational environment, the next step would depend on verified evidence, severity, business impact, and escalation procedures.

## Evidence boundary

This document describes investigation methodology practised in coursework/lab settings. It does not claim professional SOC handling, customer incidents, or fabricated detections.
