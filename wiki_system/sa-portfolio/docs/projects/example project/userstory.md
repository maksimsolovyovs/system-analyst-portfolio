#### US-01 - Routing an incomming SWIFT MT message 
As a banking integration system
I want t osend a SWIFT MT message to the routing service 
So that it is automatically routed to the appropriate internal processing system

**Acceptance criteria**
- The message is validated according to the SWIFT MT format
- The message type is determined (MT103, MT202, etc.)
- Business routing rules are applied
- The message is sent to the appropriate downstream service
- All actions are logged

---

#### US-02 - Flexible routing rule management
As an operations engineer 
I want to customize routing rules without changing code
To quickly adapt to changes in banking processes

**Acceptance Criteria**
- Rules are stored in the configuration repository
- Rule prioritization is supported
- Changes are applied without restarting the service

---

#### US-03 - Tracking Message Status
As a support representative
I want to see the processing status of SWIFT messages 
To diagnose errors and delays

**Acceptance Criteria**
- Each message has a unique ID
- Available statuses: RECEIVED, VALIDATED, ROUTED, FAILED
- Audit trail available