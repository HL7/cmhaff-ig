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