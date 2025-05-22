#### Related Regulations and Standards

- **[Integrating the Healthcare Enterprise (IHE) Audit Trail and Node Authentication (ATNA) Integration Profile.](https://www.ihe.net/Technical_Frameworks/#IT)** This IHE profile references
the **[Internet Engineering Task Force (IETF) RFC 3881 Audit Record standard](https://datatracker.ietf.org/doc/rfc3881/)**
- **[HL7 EHR Records Management and Evidentiary Support Functional Profile, Release 1 (RMES)](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=86)** Provides functions in an EHR system that can help an organization maintain a legal record for business
and disclosure purposes

#### Implementation Guidance

Every consumer mobile health app needs an audit strategy, which includes what data will be generated for audit, who will be able to access audit records,
the location where audit data is stored, the length of time audit information will be stored, and any ability to delete audit data. Audit for security events is
highly dependent on the nature of the app itself; audit requirements will differ significantly based on app sponsorship (e.g., sponsor is a HIPAA entity or a
commercial non-covered entity), the need for user authentication, and if data generated through an app is accessible by consumers, clinicians, or both.