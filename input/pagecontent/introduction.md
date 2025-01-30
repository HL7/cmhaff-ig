### Acknowledgements

The Consumer Mobile Health Application Functional Framework (cMHAFF) team acknowledges the members of the HL7
Mobile Health Workgroup, who developed this Standard for Trial Use. In addition, acknowledgements are due to the HL7
EHR Workgroup and the HL7 Security Workgroup, and the Community Based Health Services (CBHS) workgroups, which
also provided valuable guidance. Many other mobile health initiatives in the European Union and USA influenced cMHAFF
as well, as referenced throughout this specification.

### Background

As of 2021, there are thousands of consumer health applications (apps), which run on smartphones, watches, tablets, and
other mobile devices, available for download from platform-specific application stores such as the Apple App Store (iOS)
and Google Play (Android). Consumer acceptance and use of these apps is primarily based on recommendations—either
personal recommendations through individual contacts or social media or app store ratings. While this information is
important in understanding the relevance of an app to one’s life and the design and usability of an app, it is insufficient in
communicating how an app secures and protects the personal information of its users. This poses a problem both for
consumers and clinicians, who may be considering or prescribing use of an app to help track and improve health behaviors
and conditions.

There is a great diversity in consumer health apps. Some are meant to be used for oneself, some help manage care for
others, and some work best when an individual uses an app along with consultation from a health professional. Below are
three exemplary use cases of increasing complexity that are introduced and serve to guide development of cMHAFF.

### Intended Audience

1. cMHAFF is primarily directed at **developers and vendors of mobile health apps for consumers**, to assist them in building and marketing apps that educate consumers and protect their privacy, security, data access, etc.
2. cMHAFF is also directed at organizations (such as test labs, certification bodies, professional societies, or organizations that provide app reviews and ratings) that will assess or endorse mobile apps for conformance to essential criteria.
3. cMHAFF can also be informative as a checklist (or “gold standard”) for prospective purchasers of mobile apps (e.g., consumers, or providers on behalf of consumers). The beneficiaries of cMHAFF will primarily be consumers, due to improvements in apps and in a consumer’s increased understanding and trust. Other beneficiaries may include those who receive information from consumer health apps, such as providers, caregivers, and researchers. Some provider organizations, such as the American Medical Association, have published principles1 to ensure accurate, effective, safe and secure mHealth apps.

### Relationship to Other Standards

* The HL7 EHR System Functional Model and the HL7 PHR System Functional Model, and their profiles, provided inspiration for cMHAFF. While cMHAFF is not intended for EHRs and PHRs, it is similar in that it is a broad general framework that can be constrained or extended (profiled) to focus on specific realms or types of apps.
* Several European standards and guidelines for mHealth apps were analyzed and mapped to cMHAFF categories. These are included in Section 7.0, References.