#### Implementation Guidance

In the realm of alerts and notifications, the following table proposed suggested standardized (generic)terms in the left column, with mappings to the
leading two platforms in the middle columns, and comments in the right column. The platform-specific definitions have been derived from web
sources,with preference given to information from the creators of the platforms (Apple, Google). Note: the mapping cannot be made an exact 1:1. In
some cases, the platform-specific term may be more precise(e.g., subtypes) than the generic term, but we do not require a generic equivalent for
every platform- specific term. In other cases, there may be substantial similarity of concepts across platforms, but not identical behavior, and
certainly not identical appearance.
Despite the proposed granularity of these terms, that does not mean that there need to be separatecMHAFF conformance requirements for each
type, but at least the opportunity is there if the need arises. In particular, there may be different conformance requirements for “alerts” vs other
types ofnotifications.

!! Convert table !!

**Hierarchy**
- Message (overarching term)
    - Content Message (e.g., HL7 v2, C-CDA payload, FHIR resource) – out of the scope for this set of definitions.
    - Notification (overarching term)
        - Alert (requires user action, whereas all other types of notifications do not require it,though they may allow it)
        - Persistent notification
        - Temporary notification
        - Emergency Notification (government, outside app control)