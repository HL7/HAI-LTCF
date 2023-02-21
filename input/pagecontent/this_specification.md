### FHIR REST API

Submission of HAI event and summary reports from LTC facilities relies on the RESTful paradigm. Implementers need to be aware of and follow all the principles of [RESTful design](https://www.hl7.org/fhir/exchange-module.html#rest). Please refer to that section of the core FHIR spec.

### Actors

The following actors are in-scope of the expected RESTful exchange of this specification:

* Source: An application that exposes a Questionnaire to a consumer. This actor may also be the creator of the QuestionnaireResponse, but could also me an intermediary. This can be thought of as the server in a client/server interaction at a Long Term Care Facility. 
* Consumer: An application that consumes a QuestionnaireResponse instance. This can be thought of as the client in a client/server interaction. 

The HAI-LTCF FHIR specification does not define additional rules for sending/receiving information beyond what is already defined in the FHIR core spec and US Core.

### Profiles and Extensions

To claim conformance to a HAI-LTCF FHIR Profile, servers SHALL:

* Be able to populate all profile data elements that have a minimum cardinality >= 1 and/or flagged as Must Support as defined by that profile’s StructureDefinition.

The following profiles and extensions are present in the specification. Details on these profiles and extensions are available on the [Artifact Index page](artifacts.html). 

### Questionnaire/QuestionnaireResponse Profiles

* [Healthcare Associated Infection for Long Term Care Single-Person Report Questionnaire](StructureDefinition-hai-ltcf-single-person-report-questionnaire.html)
* [Healthcare Associated Infection for Long Term Care Single-Person Report QuestionnaireResponse](StructureDefinition-hai-ltcf-single-person-report-questionnaire-response.html)
* [Healthcare Associated Infection for Long Term Care Population Summary Questionnaire](StructureDefinition-hai-ltc-population-summary-questionnaire.html)
* [Healthcare Associated Infection for Long Term Care Population Summary QuestionnaireResponse](StructureDefinition-hai-ltcf-population-summary-questionnaire-response.html)

#### Questionnaire/QuestionnaireResponse Instances

* [HAI-LTCF-Questionnaire-MDRO-CDI-Event](Questionnaire-hai-ltcf-questionnaire-mdro-cdi-event.html)
* [HAI-LTCF-Questionnaireresponse-MDRO-CDI-Event](QuestionnaireResponse-hai-ltcf-questionnaireresponse-mdro-cdi-event.html)
* [HAI-LTCF-Questionnaire-MDRO-CDI-Summary](Questionnaire-hai-ltcf-questionnaire-mdro-cdi-summary.html)
* [HAI-LTCF-Questionnaireresponse-MDRO-CDI-Summary](QuestionnaireResponse-hai-ltcf-questionnaireresponse-mdro-cdi-summary.html)


### Dependence on US Core and Value Set Authoring Center

This specification relies on the US Core Patient profile to exchange single person event information. Where US Core profiles do not exist, unprofiled (base) resources are referenced. It is expected that US Core will evolve over time, and as it does this specification will be in a position to take advantage of newly profiled resources defined within US Core.
More information on US Core can be found [here](https://www.hl7.org/fhir/us/core/). 

Quesitonnaire and QuestionnaireResponses defined within this specification reference terminologies (ValueSets) defined within the Value Set Authoring Center (VSAC). OIDs for the ValueSets referenced from the Questionnaires and QuestionnaireResponses are:
* [NHSNHealthcareServiceLocationCode: 2.16.840.1.113883.13.19](https://vsac.nlm.nih.gov/valueset/2.16.840.1.113883.13.19/expansion/Latest)
* [NHSNPrimaryResidentServiceType: 2.16.840.1.113883.10.20.5.1.5.9.3](https://vsac.nlm.nih.gov/valueset/2.16.840.1.113883.10.20.5.1.5.9.3/expansion/Latest)
* [NHSNSignificantPathogenCode: 2.16.840.1.114222.4.11.3194](https://vsac.nlm.nih.gov/valueset/2.16.840.1.114222.4.11.3194/expansion/Latest)
* [NHSNSpecimenTypeCode: 2.16.840.1.114222.4.11.3249](https://vsac.nlm.nih.gov/valueset/2.16.840.1.114222.4.11.3249/expansion/Latest)


### Design Considerations

This IG specifies a FHIR Questionnaire-based approach. This approach takes advantage of the FHIR Questionnaire resource that has been designed as an organized collection of questions intended to solicit information from individuals involved in the healthcare domain. These Questionnaires closely mirror the actual NHSN forms.

The following profiles are defined in the [HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm](http://hl7.org/fhir/us/hai/2019May/index.html) and are re-used in this IG:

* The Questionnaire profile [Healthcare Associated Infection Single-Person Report Questionnaire](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-single-person-report-questionnaire) defines constraints to which all HAI NHSN single-person reports (Questionnaire instances) must conform.
* The QuestionnaireResponse profile [Healthcare Associated Infection Single-Person Report QuestionnaireResponse](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-single-person-report-questionnaire-response) defines constraints to which all responses to HAI NHSN single-person reports (QuestionnaireResponse instances) must conform.
* The Questionnaire profile [Healthcare Associated Infection Population Summary Questionnaire](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-population-summary-questionnaire) defines constraints to which all HAI NHSN population summary reports (Questionnaire instances) must conform.
* The QuestionnaireResponse profile [Healthcare Associated Infection Population Summary QuestionnaireResponse](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-population-summary-questionnaire-response) defines constraints to which all responses to HAI NHSN population summary reports (QuestionnaireResponse instances) must conform.

Note: The *HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm* containing the above profiles was balloted in the May 2019 ballot cycle. Ballot reconcillation has been completed on the ballot and the agreed changes are in progress (one change of note being that the IG is now based on FHIR R4 rather than FHIR R3). The *HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm* IG will be finalized and published before this IG is published.  

