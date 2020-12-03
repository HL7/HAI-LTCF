[Previous Page - Audience](audience.html)

This IG specifies a FHIR Questionnaire-based approach. This approach takes advantage of the FHIR Questionnaire resource that has been designed as an organized collection of questions intended to solicit information from individuals involved in the healthcare domain. These Questionnaires closely mirror the actual NHSN forms.

The following profiles are defined in the [HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm](http://hl7.org/fhir/us/hai/2019May/index.html) and are re-used in this IG:

* The Questionnaire profile [Healthcare Associated Infection Single-Person Report Questionnaire](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-single-person-report-questionnaire) defines constraints to which all HAI NHSN single-person reports (Questionnaire instances) must conform.

* The QuestionnaireResponse profile [Healthcare Associated Infection Single-Person Report QuestionnaireResponse](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-single-person-report-questionnaire-response) defines constraints to which all responses to HAI NHSN single-person reports (QuestionnaireResponse instances) must conform.

* The Questionnaire profile [Healthcare Associated Infection Population Summary Questionnaire](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-population-summary-questionnaire) defines constraints to which all HAI NHSN population summary reports (Questionnaire instances) must conform.

* The QuestionnaireResponse profile [Healthcare Associated Infection Population Summary QuestionnaireResponse](http://hl7.org/fhir/us/hai/2019May/StructureDefinition/hai-population-summary-questionnaire-response) defines constraints to which all responses to HAI NHSN population summary reports (QuestionnaireResponse instances) must conform.

Note: The *HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm* containing the above profiles was balloted in the May 2019 ballot cycle. Ballot reconcillation has been completed on the ballot and the agreed changes are in progress (one change of note being that the IG is now based on FHIR R4 rather than FHIR R3). The *HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm* IG will be finalized and published before this IG is published.  

[Next Page - References](references.html)