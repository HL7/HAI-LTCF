---
title: Design Considerations
layout: default
active: Design Considerations
---

[Previous Page](Audience.html)

This IG specifies a FHIR Questionnaire-based approach. This approach takes advantage of the FHIR Questionnaire resource that has been designed as an organized collection of questions intended to solicit information from individuals involved in the healthcare domain. This closely mirrors the actual NHSN forms.

* The Questionnaire profile [Healthcare Associated Infection Report Questionnaire](http://hl7.org/fhir/us/hai/StructureDefinition/hai-single-person-report-questionnaire) defines constraints that all HAI NHSN single-person report forms (Questionnaire instances) must conform to.

* The QuestionnaireResponse profile [Healthcare Associated Infection Report QuestionnaireResponse](http://hl7.org/fhir/us/hai/StructureDefinition/hai-single-person-report-questionnaireresponse) defines constraints that all  responses to HAI NHSN single-person report forms (QuestionnaireResponse instances) must conform to.

* TODO

[Next Page](References.html)