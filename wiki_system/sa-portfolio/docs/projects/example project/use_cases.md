#### UC-01 - Incoming MT103 Processing

**Actors**
- Core Banking System
- SWIFT Route Service
- Payment Processing Service

**Main Scenario**
1. Core Banking System sends MT103 to Route Service via MQ
2. Route Service
- Parses the message
- Validates the structure
- Determines the message type
3. Service applies routing rules
- By sender BIC
- By currency
- By transaction type
4. Message is forwarded to Payment Processing Service
5. An entry is saved in the audit log
6. A receipt confirmation is returned

**Alternative Scenarios**
- If the message is invalid → FAILED status + entry in Dead Letter Queue/ error-queue
- If the route is not found → sending to manual-review queue