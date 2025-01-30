The questions in this section help the intended audience (particularly mobile app developers and vendors) determine which
conformance subsections of cMHAFF should be read. Each subsection contains one or more conformance statements.
Based on the characteristics of the app being developed, some of those subsections may be applicable and some may not.
To assist developers in understanding which subsections of cMHAFF are relevant to their app, the following table is
presented. The left column is a yes/no question, and the right column represents decisions whether or not to apply sections
of cMHAFF, depending on the answer to that question.

... questions table

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
Figure 1. CMHAFF Sections and Mobile App Life Cycle