The questions in this section help the intended audience (particularly mobile app developers and vendors) determine which
conformance subsections of cMHAFF should be read. Each subsection contains one or more conformance statements.
Based on the characteristics of the app being developed, some of those subsections may be applicable and some may not.
To assist developers in understanding which subsections of cMHAFF are relevant to their app, the following table is
presented. The left column is a yes/no question, and the right column represents decisions whether or not to apply sections
of cMHAFF, depending on the answer to that question.

| Questions | Decisions Based on Answers |
| --- | --- |
| Which sections are mandatory for all mobile app developers, regardless of how basic the application is? | Sections covering product development, product upgrades, and downloading/installing the app are always required. |
| Does the application process information that can identify a patient? | **If yes:** Sections regarding authentication, authorization, auditing, app/data removal, and post-closure permitted uses apply.<br>**If no:** Those specific sections are not applicable. |
| Does the application save or send data externally (such as to cloud storage or another health IT system)? | **If yes:** Sections addressing data security at rest, security in transit, data authenticity/provenance, and data exchange/interoperability apply. |
| Does the application interface with external sensors or devices that collect patient health measurements? | **If yes:** Sections related to device pairing and synchronization also apply. |
| Does the application deliver notifications or alerts to the user? | **If yes:** The section governing notifications and alerts applies. |
{: .grid .table-striped}

The intent of the Mobile Health Work Group is to use this feedback to improve the quality and relevance of the Framework
so that it can be approved as a Standard for Trial Use 2 (STU) in 2023.
Each section addresses product information and technical concerns based on a given stage of the app lifecycle, through
conformance criteria, supported by references to related regulations and standards. Implementation guidance is also
included.

### Goals

The primary goals of cMHAFF are to provide a standard against which a mobile app’s foundational characteristics --
including but not limited to security, privacy, data access, data export, and transparency/disclosure of conditions -- can be
assessed. The framework is based on the lifecycle of an app, as experienced by an individual consumer, from first deciding
to download an app, to determining what happens with consumer data after the app has been deleted from a smartphone.
It is important to note that the Framework does not speak directly to the specific health or clinical functionality of an app but
can be extended to do so through the use of profiles (with constraints and/or extensions) developed on top of cMHAFF.
The decision to create a standard focused on a smaller set of criteria was made so that the standard is both developer-
friendly and easy to update on a frequent basis. CMHAFF challenges market assumptions concerning safe and acceptable
use of personal information and may in some circumstances increase coding complexity and decrease the efficiency of data
transmission. As such, there is no expectation that most consumer health apps will choose to follow this standard. Yet, for
apps which conform, cMHAFF can potentially provide a path to assessments that can span a range including self-attestation,
testing, endorsement 2 , and/or certification (voluntary or regulatory). CMHAFF is independent of the method of assessment
but aims to be suitable for use for types of assessments up to and including certification. Certified apps can promote their
conformance, and as a consequence, consumers who use the apps, and providers who recommend them, can be more
confident of an app’s rigor in enforcing basic security, its respect for the privacy of individuals, and the usefulness of data
for improving and maintaining a better state of health.

### Scope

CMHAFF focuses specifically on consumer mobile apps that run on devices such as smartphones, tablets, and wearables.
With that said, it is understood that “mobile” is relative and so in certain circumstances health apps running on laptops,
desktops, etc, may also be included. It is focused on the general capabilities, that can be thought of as “horizontal” features
that are applicable to most or all apps, rather than to the specific health, clinical, or medical functionality of an app.
There is a broad range of apps that cMHAFF intends to cover, from simple self-contained standalone apps that a consumer
can use for personal benefit, which do not exchange or store data outside the mobile device; to apps that share or store
data externally (e.g., in the app provider’s cloud) but do not interact directly with provider systems; to systems that share
and store data externally and interact with provider EHRs or organizations (in the USA, covered entities or business associates governed by HIPAA and/or FDA).

The intent is to lay a foundation, on top of which realm-specific and domain-specific “profiles” can be layered, that addresses
an app’s:
* Product Information for consumers (e.g., App Store descriptions, product disclosures)
* Security
* Privacy
* Permission to use device features
* Data Access
* Data Sharing
* Terms of Use, Conditions
* Product Development, including risk management, user-centered design, compliance with applicable regulations, functions (product description), reliability, performance, scalability, safety, compatibility, and portability.

### Out of Scope

* “Professional” apps that may run on consumer devices, but are intended for healthcare workers, e.g., clinical
decision support aids, which are exclusively not consumer-focused.
* Clinical functionality of health apps (e.g., diabetes monitoring, exercise calculations). The Mobile Health workgroup does not have the subject matter expertise to define clinical-level types of criteria. These types of criteria would be outlined within specific implementation guides for use of consumer health apps in respective domains.
* General “device” security requirements, e.g., password or biometric locking of a phone. CMHAFF is an application functional framework intended for app developers, not a framework for the devices or platforms on which the apps run. As such, cMHAFF is not directed to Apple, Google, Samsung, or other device manufacturers and in general, seeks to remain agnostic in terms of platform. However, risk management should identify dependencies or assumptions about the common platforms that an app may rely on.
* General “infrastructure” requirements for consumers or healthcare organizations, such as the protection of networks via virus or malware protection, firewalls, etc., physical environmental security, since app developers have no control over such networks or environments. However, risk management should identify dependencies or assumptions about the supporting infrastructure that an app may rely on and should identify threats and mitigate risks.
* Human resource policies and procedures of developers, healthcare organizations, or consumers, such as security awareness education, except inasmuch as they directly affect product development.

### Conformance Design Principles

Conformance Criteria in the following sections follow a lifecycle model in relation to a consumer’s use of a mobile health
application, from first finding an app in an App Store to disuse and de-installation.

<div>
{% include img.html img="HL7-CMHAFF-Workflow-2026.png" width="70%" %}
</div>
Figure 1. CMHAFF Sections and Mobile App Life Cycle

### General Considerations

Each section is a category of criteria that follows a common format. First, there is a brief non- normative description of the category. Then there is a subsection containing a normative table of conformance criteria. Some criteria are applicable to all consumer health apps and other criteria are to be applied conditionally based on the functionality and scope of an app. For example, some apps do not transmit personal data to a source outside of the smartphone, while some integrate with external data sources; some apps integrate with medical and wellness devices, while others do not. Criteria are separated from “force”. That is, each criterion stated in a neutral way, and the optionality of addressing the criteria while claiming conformance to the standard, is in a separate column. The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED”, “MAY", and "OPTIONAL" in this document are to be interpreted as described in Internet Engineering Task Force (IETF) RFC 2119. Force follows this convention:

* **SHALL** - The definition is an absolute requirement of the specification
* **SHOULD** - This word, or the adjective "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
* **MAY** - This word, or the adjective "OPTIONAL", mean that an item is truly optional. One vendor may choose to include the item because a particular marketplace requires it or because the vendor feels that it enhances the product while another vendor may omit the same item. An implementation which does not include a particular option MUST be prepared to interoperate with another implementation which does include the option, though perhaps with reduced functionality. In the same vein an implementation which does include a particular option MUST be prepared to interoperate with another implementation which does not include the option (except, of course, for the feature the option provides.)
* **[IF]** - The stated force applies only when the clause in brackets is applicable to the product. When the
clause does not apply, no conformance is expected.

Following the table of conformance criteria, there are two non-normative subsections that provide optional
guidance:

* _**Related regulations and standards:**_ References to documents which can help an app developer or vendor are included. Regulations, standards and guidelines are cited here only if they are the direct source of a conformance criterion: otherwise, then they are listed in the Appendices (section 6.1, Reference Documents). To avoid redundant listings, any referenced document (with its URL) is only listed in the first relevant subsection: subsequent references are abbreviated and placed in footnotes. No regulations are cited as normative in cMHAFF, because they are realm-specific. NOTE: Legislation and regulations will vary between realms (locations) internationally and even within a country (e.g., states or provinces). Applicable regulations take precedence over cMHAFF when overlap or discrepancies exist. CMHAFF does not replace or override regulations of a realm.
* _**Implementation guidance:**_ Guidance for app developers is included. As applicable, the differential application of conformance criteria by type of app is discussed, referencing the exemplary use cases described previously.