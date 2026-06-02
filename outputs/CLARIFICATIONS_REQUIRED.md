# Clarifications Required - Loan Against Life Insurance Policies

## Critical Clarifications
1. **System screen inventory missing:** Requirement document defines business rules but does not define exact UI screens, navigation paths, or screen ownership across roles.
2. **Role-action matrix missing:** Exact permission mapping for Branch Maker, Assistant Branch Manager, Branch Manager, Sanctioning Authority, Operations, and Monitoring users is not explicitly defined.
3. **Validation message catalog missing:** Expected error/success alert texts and localization rules are not provided.
4. **Field specification gaps:** No explicit field-level constraints (min/max length, accepted character sets, masking, default values) are provided for key input fields.
5. **Integration contract details missing:** API/channel details, response codes, retry limits, timeout thresholds, and fallback handling are not specified for insurer/CIBIL/RBI/CFR/KYC/FEMA integrations.
6. **Status transition matrix missing:** Full state machine with allowed forward/reverse transitions, manual overrides, and rejection reopen behavior is not specified.
7. **Notice dispatch mechanism unclear:** Trigger batch timings, holiday handling, postal proof capture, and re-dispatch rules are not defined.
8. **Accounting treatment details missing:** Exact GL postings for proceeds appropriation, expense recovery, and excess credit transfer are not documented.
9. **Document policy unclear:** Allowed file types/sizes/versioning/e-sign requirements for uploaded documents are not provided.
10. **Audit and reporting requirements incomplete:** Required MIS reports, download format, retention period, and audit export structure are not specified.

## Assumptions Used For Test Case Generation
- A centralized loan processing application exists with screen-wise workflow from application to closure.
- Product has distinct workflow stages and status values visible in list and detail pages.
- Maker-checker controls and role-based authorization are implemented.
- Integrations are synchronous/asynchronous with retriable failure handling.
- Standard banking validations (mandatory checks, duplicate prevention, audit trail, and timestamped actions) apply.
