As noted in the Introduction, consumer mobile heath apps take many forms, and as such, conformance statements in
this standard must allow for variation based on multiple factors, including data sensitivity, the nature of conditions
addressed by the app (e.g., wellness, chronic illness), and whether/how app data connect to other data sources.
In this section, three archetypal use cases are introduced. While most consumer mobile health apps will not precisely fit
any of these models, the models are meant to demonstrate a continuum of issues which may be applied to any app. Use
Case A covers the least sensitive example of a health app that collects user information, while Use Case B builds off of
Case A with the inclusion of an external system through which personal data is synchronized with the device. Use Case
C is the most sophisticated and generates the most requirements. Its description includes examples of the risk factors
that should be considered by developers and users.
The Conformance Criteria section includes discussion of considerations as to how subsets of conformance criteria can
be addressed in different manners, referencing the use cases in this section as a way to provide directional, rather than
pinpoint, guidance.

### Use Case A: Simple, Standalone

In this use case example a walking app collects data based on how far someone walks, using things such as
accelerometers and GPS technology. In this app a consumer can view aspects such as a history of walks taken and
summary statistics related to distance walked and estimated calories burned, etc. In this U.S.-based use case the App
developer is not a HIPAA-covered 3 entity (CE) such as a healthcare provider, nor is the app a business associate of a CE
(such as a hospital or physician). This type of app might be generally available in a mobile app store (e.g., Apple, Android)
and downloaded by a consumer/patient for personal use.

<div>
{% include img.html img="HL7-CMHAFF-Use-Case-A-2026.png" width="70%" %}
</div>

|  | Simple |
| --- | --- |
| **Medical Device App Categorization** | Wellness |
| **Data Device Categorization** | None |
| **PHI Data Storage** | Smartphone |
| **Data transmission by App** | None |
| **Importance of Data Integrity** | Low |
| **(USA) HIPAA covered?** | No |
{: .grid .table-striped}

### Use Case B: Device-Connected Wellness App

In this health app use case a weight management app is used to help consumers to systematically collect weight
information, food consumption information and exercise information. Weight can be entered manually, or a consumer can
link a wireless scale to the app so that weight is automatically collected when using the scale. Food consumption is entered
manually, and the tool estimates calories consumed based on the consumer’s input. Exercise information may be entered
manually or collected automatically through integration with a smart watch. The app analyzes all the data and offers
warnings and advice (e.g., patient’s unhealthy combination of weight and exercise levels lead to recommendations for diet
and exercise changes). In the U.S., these types of apps, depending on their use and context could fall under FDA guidelines
for Software as a Medical Device (SaMD) 1 designation, but if the health app is generally providing low-risk health lifestyle
recommendations, then it would not be interpreted as a SaMD 2 . In this example, the app has an ability to download weight,
activity, and food consumption information into a patient-managed personal health record (PHR) system through a
published API. In the US Realm, the App developer is not a HIPAA entity, but an app developer may enter into a HIPAA
business associate agreement with a covered entity and be offered to patients through an approved app store or EHR-
based integration.

<div>
{% include img.html img="HL7-CMHAFF-Use-Case-B-2026.png" width="70%" %}
</div>

|  | Device-Integrated Application |
| --- | --- |
| **App Category (Medical Device)** | Wellness |
| **Connected Device Category** | Either regulated or unregulated hardware |
| **Location of PHI Storage** | Mobile device or personal health record (PHR) |
| **App Data Transfer Path** | Flows from device to app to PHR |
| **Data Integrity Priority** | Moderate to high |
| **Subject to US HIPAA Regulations?** | Varies; contingent on whether a covered entity owns the PHR |
{: .grid .table-striped}

### Use Case C: EHR-Integrated Disease Management App

In this use case we provide the example of a diabetes management app that allows a consumer to collect blood sugar
readings through a Bluetooth-enabled glucometer. A healthcare provider prescribes the app to enable the patient’s blood
sugar to be captured through devices, rather than relying on manual entry by the patient, and to electronically transmit the
readings to the patient’s physician, rather than using paper or FAX. Activity data are collected through an activity tracker,
and a consumer can open the app to record meals and snacks to enable estimates of caloric consumption. This type of
Collected data is automatically “pushed” to a third-party cloud-based platform. The patient is aware of the cloud, though
not familiar in detail with how data are protected in transit or storage. When a consumer views information in the app,
which shows daily glucometer readings and related information, this information is “pulled” in but does not persist on the
smartphone when the app is closed. It is also possible for the consumer to directly enter blood sugar readings (e.g., if
Bluetooth connection is not working). From the cloud platform, consumer information is “pushed” to a provider’s
Electronic Health Record (EHR), where it is accepted as Patient Generated Health Data (PGHD), according to the
preferences of the patient and the policies of the provider. From the EHR, a physician can define logic to assess blood
sugar readings such that the consumer is alerted through the app when a measurement is out of range or when a set
number of high or low readings are noted within a prescribed period of time.

<div>
{% include img.html img="HL7-CMHAFF-Use-Case-C-2026.png" width="70%" %}
</div>

|  | EHR-Integrated Application |
| --- | --- |
| **App Category (Medical Device)** | Medical |
| **Connected Device Category** | Regulated hardware |
| **Location of PHI Storage** | Cloud or electronic health record (EHR) |
| **App Data Transfer Path** | Flows from device to app to cloud to EHR |
| **Data Integrity Priority** | High |
| **Subject to US HIPAA Regulations?** | Yes |
{: .grid .table-striped}

### Risk Factors

For apps, especially those like Use Case C, there are several potential threats and vulnerabilities which should be
assessed and mitigated, where necessary, by mHealth developers (see Product Risk Assessment and Mitigation). While
cMHAFF does not attempt to “do” the risk assessment for any particular mobile app, the following are examples of
specific risk scenarios that may be applicable and point to cMHAFF criteria (potential mitigations are listed in
parentheses). Some of these potential risks are motivators for the conformance criteria in cMHAFF. Where risks have
both high likelihood and high impact, SHALL criteria are indicated.

| Risk Factor | Conformance Section |
| --- | --- |
| Losing a device that stores confidential app data exposes sensitive information (mitigated via data encryption and automatic timeout/logoff). | App and Data Removal |
| Losing or damaging a device prevents app access and disrupts care, even when privacy remains intact (addressed via data backup information and restoration to a replacement device). | Product Information |
| Enabling convenience features like "automatic login" or "remember me" allows access without re-authentication (avoid offering this option if the app processes Protected Health Information). | Authentication |
| Leaving an unlocked device unattended with the app open allows unauthorized viewing (mitigated by automatic timeout/logoff). | Authentication |
| Inaccurately recorded or transmitted health measurements can lead consumers to make harmful decisions (mitigated through quality management and evidence disclosure). | Product Risk Assessment |
| Pairing a measurement device with a smartphone that belongs to a different user risks associating data with the wrong person (addressed via pairing user accounts). | Authentication |
| Relying on third-party cloud platforms with weak, undisclosed security exposes stored data (mitigated by disclosing infrastructure safeguards), while transfers between the app and cloud may lack adequate protection (mitigated by encrypting data in transit). | Security for Data at Rest |
| Replacing or discontinuing use of a mobile device without wiping local and externally transmitted data leaves information exposed (covered by app/data removal and post-closure permitted data uses). | App and Data Removal |
| Receiving healthcare providers lack control over consumer device specs, environments, and usage habits compared to managed enterprise hardware (out of developer scope, though it should be noted in the product risk assessment). | Product Risk Assessment |
{: .grid .table-striped}

### Environmental Scan

The documents mentioned below are not standards, but explain the state of the mobile health industry in the USA and
Europe, and assist developers to understand which legislation is applicable to their apps.

* [Journal of Medical Internet Research: mHealth and Mobile Medical Apps: A Framework to Assess Risk and Promote Safer Use](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4180335/)
* [HIMSS Interoperability Environmental Scan](https://www.himss.org/environmental-scan)
* [ONC Patient-Generated Health Data resources and references](https://www.healthit.gov/topic/scientific-initiatives/patient-generated-health-data). This addresses opportunities and challenges for patient-generated health data (PGHD) and their use by clinicians. Much PGHD could come from mobile devices.
* [Good Practice Guidelines on Health Apps and Smart Devices (Mobile Health or mHealth)](https://www.has-sante.fr/portail/upload/docs/application/pdf/2017-03/dir1/good_practice_guidelines_on_health_apps_and_smart_devices_mobile_health_or_mhealth.pdf). While this is written for France, and influenced many of the criteria in cMHAFF, it also contains an extensive literature search and references that serve as an environmental scan.