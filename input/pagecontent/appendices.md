### CMHAFF Pilots

Three pilots were conducted in relation to the CMHAFF STU:
* Children’s Hospital of Philadelphia
* Health App Analyzer– HRSA HITEQ
* CEN/ISO Health & Wellness Apps

Pilot Documentation: https://confluence.hl7.org/display/MH/cMHAFF+Pilot+Implementations

### Reference Documents

| Document | Relevance to CMHAFF |
| --- | --- |
| [ONC API Task Force Final Report](https://www.healthit.gov/facas/sites/faca/files/HITJC_APITF_Recommendations.pdf) | General, Authentication, Authorization | 
| [ONC Model Privacy Notice (updated December, 2016)](https://www.healthit.gov/sites/default/files/2016_model_privacy_notice.pdf) | Authorization for Data Collection and Use |
| [Open Web Application Security Project (OWASP) Top 10 Mobile Security Risks](https://www.owasp.org/index.php/Mobile_Top_10_2016-Top_10) | Risk Assessment and Mitigation, Authentication, Authorization, Security for Data at Rest, Security for Data in Transit | 
| [U.S. Department of Health and Human Services, Usability Guidelines, U.S. Dept. of Health and Human Services. The Research-Based Web Design & Usability Guidelines, Enlarged/Expanded edition. Washington: U.S. Government Printing Office, 2006.](https://www.usability.gov/sites/default/files/documents/guidelines_book.pdf) | Usability | 
| [US Department of Health and Human Services (HHS) Summary of the HIPAA PrivacyRule](https://www.hhs.gov/hipaa/for-professionals/privacy/laws-regulations/) which includes a definition of PHI (also known as “individually identifiable health information”) for the US realm. | Launch App and Establish User Account | 
| [U.S. Federal Trade Commission, Children’s Online Privacy Protection Rule (COPPA)](https://www.ftc.gov/tips-advice/business-center/guidance/complying-coppa-frequently-askedquestions) for the US realm. National Institute of Standards and Technology, Electronic Authentication Guideline, NIST 800-63-2. | Launch App and Establish User Account | 
| [U.S. Food and Drug Administration. Applying Human Factors and Usability Engineering to Medical Devices. February, 2016.](https://www.fda.gov/downloads/MedicalDevices/.../UCM259760.pdf) | Usability | 
| [U.S. Food and Drug Administration: Device Software Functions Including Mobile Medical Applications](https://www.fda.gov/medical-devices/digital-health-center-excellence/device-software-functionsincluding-mobile-medical-applications). <br/>[FDA Policy for Device Software Functions and Mobile Medical Applications, updated 9/26/2019](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/policy-device-softwarefunctions-and-mobile-medical-applications) | Regulatory Considerations | 
| [U.S. Food and Drug Administration (FDA) – FDASIA Health IT Report.](https://www.fda.gov/downloads/AboutFDA/CentersOffices/OfficeofMedicalProductsandTobacco/CDRH/CDRHReports/UCM391521.pdf) | Risk Assessment andMitigation | 
| [U.S. Food and Drug Administration: Cybersecurity](https://www.fda.gov/medical-devices/digital-healthcenter-excellence/cybersecurity) | Risk Assessment and Mitigation | 
| [U.S. Food and Drug Administration (FDA) Digital Health Innovation Action Plan](https://www.fda.gov/downloads/MedicalDevices/DigitalHealth/UCM568735.pdf) Indicates where FDA will and will not focus its regulations of mobile health apps. | Regulatory Considerations | 
| [W3C User Agent Accessibility Guidelines (UAAG) Overview](https://www.w3.org/WAI/intro/uaag.php)<br/>[W3C Mobile Accessibility: How WCAG 2.0 and Other W3C/WAI Guidelines Apply to Mobile](http://www.w3.org/TR/mobile-accessibility-mapping/) | Usability | 
| [W3C Mobile Usability](http://www.w3.org/WAI/mobile/) | Usability | 
{: .grid .table-striped}

### Label

It is possible that cMHAFF can assist both consumers (purchasers, users) of MH apps, as well as assessment organizations, through a “Label” that summarizes the major facts about the product. Well known examples (shown below) include Nutrition Facts labels and OTC Drug Facts labels
required by governmental agencies. For cMHAFF, each “topic” (the sections of conformance criteria) would be represented by an entry, for example a table. We envision an easy-to-understand combination of graphical symbols and colors (red = bad/fail, yellow = middle/partial, green = good/present, gray = not applicable). The label’s information would be provided by a combination of self-attestation (by the app provider) verified by a third party (e.g., assessment or certification body), and possibly supplemented bythird party testing (e.g., technical requirements for interoperability, security, etc.).

To be understandable, the Label should present cMHAFF categories in consumer-friendly language, notthe developer-centric terms used for the
cMHAFF categories.

!! Label IMAGE !!

**Proposed cMHAFF Information Label for an App**

The “Ind” column is an indicator (score) for the category, summarized by a color and a graphical symbol (green/up arrow = pass, red/down arrow=fail, yellow/side arrow=middle/partial). For “not applicable, cells are shaded gray and … is proposed as a graphical symbol.

**SIMPLIFIED cMHAFF LABEL (LUMPING OF CATEGORIES)**

 <table class="grid">
        <thead>
            <tr>
                <td colspan="2"><strong>App Name:</strong></td>
                <td colspan="2"><strong>Publisher:</strong></td>
            </tr>
            <tr>
                <td><strong>Category</strong></td>
                <td><strong>Ind</strong></td>
                <td colspan="2"><strong>Other Contents (examples)</strong></td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1. Product Information</td>
                <td style="background-color: #ffcccc;">&#x25A0;</td>
                <td colspan="2">Missing information on authors of app and evidence for app claims</td>
            </tr>
            <tr>
                <td>2. Starting an Account</td>
                <td style="background-color: #ccffcc;">&#x25A0;</td>
                <td colspan="2"></td>
            </tr>
            <tr>
                <td>3. Security and Trust</td>
                <td style="background-color: #ffffcc;">&#x25A0;</td>
                <td colspan="2"></td>
            </tr>
            <tr>
                <td>4. Exchanging or Sharing Data</td>
                <td style="background-color: #cccccc;">...</td>
                <td colspan="2">App does not share data</td>
            </tr>
            <tr>
                <td>5. Ongoing Support and Updates</td>
                <td style="background-color: #ffffcc;">&#x25A0;</td>
                <td colspan="2"></td>
            </tr>
            <tr>
                <td>6. Notifications and Alerts</td>
                <td style="background-color: #ccffcc;">&#x25A0;</td>
                <td colspan="2"></td>
            </tr>
            <tr>
                <td>7. Ending Use of the App</td>
                <td style="background-color: #ffcccc;">&#x25A0;</td>
                <td colspan="2">Does not ask user about keeping or deleting data.</td>
            </tr>
            <tr>
                <td>8. Product Development Process</td>
                <td style="background-color: #ccffcc;">&#x25A0;</td>
                <td colspan="2">"Follows all applicable laws recommended by FTC Mobile Health Tool"</td>
            </tr>
        </tbody>
    </table>

Other icons, as alternatives to up/down arrows, include !! IMAGE !! or !! IMAGE !! 
The goal is to be internationally recognizable unlike letters, the meaning of which may be locale-specific.
Notes on Categories and Potential Assessment Methods The category name is listed first (followed by the corresponding cMHAFF section names in parentheses). Then there is a consumer-friendly explanation of what that section includes, and finally a recommended means of assessment.
Principles of assessment:
- Green = all SHALL and SHALL [IF] statements met (where the [IF] conditions apply), plus some “subset of SHOULD criteria” (to be determined:
may be some specific set of criteria, or some percentage).
-  Yellow = Not all of the “subset of SHOULD criteria” were met. (This is the fuzziest area. It is “clean” if all SHOULD criteria are required for green, but that may be too tough)
- Red = one or more SHALL or applicable SHALL [IF] statements were not met

Notes on how measured (self-attestation, test, inspection, etc.).


