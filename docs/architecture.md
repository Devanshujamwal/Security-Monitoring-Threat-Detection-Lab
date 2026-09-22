# Monitoring Architecture Notes

This document expands the conceptual monitoring flow used in the case study.

## Logical flow

```text
Windows endpoint ----+
                     |
Linux endpoint ------+--> Event collection --> Wazuh / SIEM --> Alert --> Triage
                     |                                      |
Network telemetry ---+                                      v
                                                     Investigation
```

## Endpoint sources

Windows and Linux systems can generate authentication, process, service, and system events. The usefulness of an alert depends on whether the underlying telemetry is complete and correctly timestamped.

## Centralized monitoring

A SIEM workflow centralizes events so related activity can be reviewed together. Centralization does not automatically make an alert correct; context still needs to be validated.

## Network context

Packet captures and firewall/security-policy information can help answer questions that endpoint logs alone cannot, such as whether a connection was attempted, allowed, blocked, or routed as expected.

## Investigation flow

A practical investigation moves from:

1. alert or observation;
2. source validation;
3. timestamp validation;
4. endpoint context;
5. network context;
6. related events;
7. documented conclusion.

## Scope

This is a learning architecture. It does not represent a production SOC, real customer environment, or claimed incident-response engagement.
