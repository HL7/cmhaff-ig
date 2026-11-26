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

| Suggested "standardized" (generic) term for cMHAFF | Apple (iOS) equivalent | Google (Android OS) equivalent | Comments |
| --- | --- | --- | --- |
| **Message**<br>Refers to any communication between computers or between a computer and a human interface via sensory or neural channels. In interoperability contexts, this specifically denotes computer-to-computer data exchanges, including transfers between distinct software programs (like APIs) running on the same hardware. | Typically refers to communication within dedicated messaging apps, such as email, SMS, instant messaging, or social media platforms. | Typically describes data packages sent from one device or server to another. | Serves as cMHAFF's broad umbrella term for data packages transmitted by applications. While alerts and notifications fall under this umbrella, "message" generally refers to in-app content rather than system alerts. In Health IT (HL7), structured messaging formats (e.g., HL7 v2) also carry clinical data and Protected Health Information (PHI). |
| **Notification**<br>A device-level communication alerting a user to significant app or system events; may or may not require user interaction. | "Notification" is used broadly to encompass various alert styles. | "Notification" serves as an umbrella term for multiple alert formats. | A broad category containing several subtypes. Although Health IT uses "notifications" for system-to-system app delivery, cMHAFF adopts a user-facing definition focused on human recipients. |
| **Alert**<br>A high-priority notification that interrupts user activity and demands an explicit response (such as tapping OK on a modal pop-up) before the user can continue using the device. | Alert | Alert Dialog (also known as Dialog Notification) | Guaranteed to be seen unless the device is powered off or the user ignores the screen. Considered higher severity than standard notifications, often triggering stricter regulatory or local policy requirements. |
| **Persistent Notification**<br>A device-level notice about important app or system activity that stays visible until the user actively dismisses it or resolves the underlying event (e.g., reading an email or text). | Notifications (within Notification Center) and Badges (on individual app icons) | Status Notification (appears outside the app window to draw the user back into the application) | Android supports multiple distinct notification formats. |
| **Temporary Notification**<br>A subtype of notification that appears on screen briefly before automatically disappearing. | Banner (and Lock Screen Notifications, which resemble banners displayed on the lock screen) | Toast (appears strictly inside the active app window, never outside it) | Because these fade away quickly, users may easily miss them. Unlike Android Toasts, iOS banners can appear outside the originating app. |
| **Emergency Notification**<br>An alert originating from an external authority (such as government agencies) to warn users of local emergencies, disasters, or severe weather. | Government Alerts on iPhone, split into two categories: "AMBER Alerts" and "Emergency Alerts." | Divided into four categories: presidential notifications, imminent extreme notifications, imminent severe alerts, and AMBER alerts (all configurable except presidential alerts). | Fall outside the scope of mobile health app development since they are not authored by app developers, though devices can be configured to display them. Included in the framework simply to avoid terminology overlap. |
{: .grid .table-striped}

**Hierarchy**
- Message (overarching term)
    - Content Message (e.g., HL7 v2, C-CDA payload, FHIR resource) – out of the scope for this set of definitions.
    - Notification (overarching term)
        - Alert (requires user action, whereas all other types of notifications do not require it,though they may allow it)
        - Persistent notification
        - Temporary notification
        - Emergency Notification (government, outside app control)