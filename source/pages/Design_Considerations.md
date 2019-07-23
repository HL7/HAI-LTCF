---
title: Design Considerations
layout: default
active: Design Considerations
---

[Previous Page](Audience.html)

This IG specifies a FHIR Questionnaire-based approach. This approach takes advantage of the FHIR Questionnaire resource that has been designed as an organized collection of questions intended to solicit information from individuals involved in the healthcare domain. This closely mirrors the actual NHSN forms.

The following profiles are defined in the [HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm](http://hl7.org/fhir/us/hai/index.html) and are re-used in this IG:

* The Questionnaire profile [Healthcare Associated Infection Report Questionnaire](http://hl7.org/fhir/us/hai/StructureDefinition/hai-single-person-report-questionnaire) defines constraints to which all HAI NHSN single-person report forms (Questionnaire instances) must conform.

* The QuestionnaireResponse profile [Healthcare Associated Infection Report QuestionnaireResponse](http://hl7.org/fhir/us/hai/StructureDefinition/hai-single-person-report-questionnaireresponse) defines constraints to which all  responses to HAI NHSN single-person report forms (QuestionnaireResponse instances) must conform.

[Next Page](References.html)