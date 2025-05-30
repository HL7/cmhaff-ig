### This Project

...

<div class="note-to-balloters" markdown="1">
**Targetting May 2025 ballot**
This is the first publication of the Consumer Mobile Health Application Functional Framework (CMHAFF) using the Common HL7 Toolset (FHIR IG Tooling).

For the September 2021 HL7 ballot, reviewers were asked to:
1. Make recommendations concerning conformance criteria, particularly the SHALL vs SHOULD vs MAY
2. Extend lists of resource references, including references to other normative and emerging standards
3. Review the framework for broad applicability and ability to be profiled in different countries.
</div>

### Introduction

Start here: [Introduction section](introduction.html).

### Function List Component Descriptions

The Function List (see [artifacts](artifacts.html)) includes the following components:

| FM Element | Requirements element | Description |
| --- | --- | --- |
| Function ID # <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a> | [id](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.id) | This is the unique identifier of a function in the Function List (e.g. CP.1.1) and should be used to uniquely identify the function when referencing functions. The Function ID also serves to identify the section within which the function exists (CP = Care Provision Section) and the hierarchy or relationship between functions (CP.1.1 is a sibling to CP.1.2, parent of CP.1.1.1 and child of CP.1). In many cases the parent is fully expressed by the children. |
| Function Type <a href="https://hl7.org/fhir/versions.html#std-process" title="Informative Content" class="informative-flag">I</a> | [meta.profile](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.meta.profile) | Indication of the line item as being a header (H) or function (F) or conformance criteria. |
| Header / Function Name <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a> | [title](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.title)  | This is the name of the Function and whilst expected to be unique within the Function List; it is not recommended to be used to identify the function without being accompanied by the Function ID.<br/>Example: Manage Medication List |
| Function Statement <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a> | [description](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.description) | This is a brief statement of the purpose of this function. Whist not restricted to the use of structured language that is used in the Conformance Criteria (see below); the Statement should clearly identify the purpose and scope of the function.<br/>Example: Create and maintain patient-specific medication lists.|
| Description <a href="https://hl7.org/fhir/versions.html#std-process" title="Informative Content" class="informative-flag">I</a> | [purpose](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.purpose) | This is a more detailed description of the function, including examples if needed.<br/>Example: Medication  lists are managed over time, whether over the course of a visit or stay, or the lifetime of a patient. All pertinent dates, including medication start, modification, and end dates are stored. The entire medication history for any medication, including alternative supplements and herbal medications, is viewable. Medication lists are not limited to medication orders recorded by providers, but may include, for example, pharmacy dispense/supply records, patient-reported medications and additional information such as age specific dosage. |
| Conformance Criteria <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a> | [statement.requirement](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.statement.requirement)  | Each function in the Function List includes one or more Conformance Criteria. A Conformance Criteria, which exists as normative language in this standard, defines the requirements for conforming to the function. The language used to express a conformance criterion is highly structured with standardized components with set meanings. The structured language used to define conformance clauses in the Function List are defined in the Glossary (Chapter 4).
| R1.1 Reference <a href="https://hl7.org/fhir/versions.html#std-process" title="Informative Content" class="informative-flag">I</a> | [statement.derivedFrom](https://hl7.org/fhir/R5/requirements-definitions.html#Requirements.statement.derivedFrom) | Reference to the previous version of the Functional Model is included to support transition from one version to the next. The first 2 digits indicate the source document; FM = Functional Model, LM = Lifecycle Model. The remainder of the reference is to the function and, if applicable, conformance criteria.
| Change Indicator | *derive or extension?* | The change indicator shows the change from previous versions. This will be valued as follows: <br/>C - Changed<br/>D - Deleted<br/>N - New<br/>NC - No Change |

### Mobile Health WG CoChairs and Publishing Facilitators

| Role  | Name | Organization | Contact |
| --- | --- | --- | --- |
| **Co-Chair** | Nathan Botts, PhD, MSIS | Westat |  |
| **Co-Chair** | Frank Ploeg | UMCG |  |
| **Co-Chair** | Gora Datta | Cal2Cal |  |
| **Co-Chair** | Matthew Graham | Mayo Clinic |  |
| **Publishing Facilitator** | Michael van der Zel BSc | UMCG | m.van.der.zel@umcg.nl |