# Lab 3 — Architecture Notes

## Architecture selected
**Layered Architecture**

### Why
1. The system has distinct presentation, business-rule, and data responsibilities.
2. Consent validation and provider verification are business rules that should be centralized and consistently enforced.
3. Separating data access helps protect health-record storage behind controlled service interfaces.
4. Audit logging can be handled as a dedicated business/data capability without coupling the user interface directly to storage.

## Main components
1. Patient Portal
2. Consent Management Service
3. Provider Verification Service
4. Record Access Service
5. Audit Service
6. Health Record Repository

## Main interfaces
- Patient Portal → Consent Management Service: Consent API
- Patient Portal → Record Access Service: Access/Status API
- Consent Management Service → Provider Verification Service: Provider Verification API
- Record Access Service → Consent Management Service: Consent Validation API
- Record Access Service → Health Record Repository: Record Query API
- Consent Management Service → Audit Service: Consent Audit API
- Record Access Service → Audit Service: Access Audit API

## Security considerations
Consent must be checked before record access. Provider verification and authorization rules are enforced in the service layer rather than relying on the presentation layer.

## Performance consideration
Keeping consent validation and record-access operations behind focused services allows frequently used validation operations to be optimized independently and avoids unnecessary access to the underlying health-record repository.
