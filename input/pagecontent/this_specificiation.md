[Previous Page - Mappings](mappings.html)

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

#### Questionnaire/QuestionnaireResponse Profiles
* [Healthcare Associated Infection for Long Term Care Single-Person Report Questionnaire](http://hl7.org/fhir/us/hai-ltcf/StructureDefinition/hai-ltcf-single-person-report-questionnaire.html)
* [Healthcare Associated Infection for Long Term Care Single-Person Report QuestionnaireResponse](http://hl7.org/fhir/us/hai-ltcf/StructureDefinition/hai-ltcf-single-person-report-questionnaire-response.html)
* [Healthcare Associated Infection for Long Term Care Population Summary Questionnaire](http://hl7.org/fhir/us/hai-ltcf/StructureDefinition/hai-ltc-population-summary-questionnaire.html)
* [Healthcare Associated Infection for Long Term Care Population Summary QuestionnaireResponse](http://hl7.org/fhir/us/hai-ltcf/StructureDefinition/hai-ltcf-population-summary-questionnaire-response.html)


#### Questionnaire/QuestionnaireResponse Instances 

* [HAI-LTCF-Questionnaire-MDRO-CDI-Event](http://hl7.org/fhir/us/hai-ltcf/Questionnaire/hai-ltcf-questionnaire-mdro-cdi-event.html)
* [HAI-LTCF-Questionnaireresponse-MDRO-CDI-Event](http://hl7.org/fhir/us/hai-ltcf/QuestionnaireResponse/hai-ltcf-questionnaireresponse-mdro-cdi-event.html)
* [HAI-LTCF-Questionnaire-MDRO-CDI-Summary](http://hl7.org/fhir/us/hai-ltcf/Questionnaire/hai-ltcf-questionnaire-mdro-cdi-summary.html)
* [HAI-LTCF-Questionnaireresponse-MDRO-CDI-Summary](http://hl7.org/fhir/us/hai-ltcf/QuestionnaireResponse/hai-ltcf-questionnaireresponse-mdro-cdi-summary.html)


#### Dependence on US Core and Value Set Authoring Center 

This specification relies on the US Core Patient profile to exchange single person event information. Where US Core profiles do not exist, unprofiled (base) resources are referenced. It is expected that US Core will evolve over time, and as it does this specification will be in a position to take advantage of newly profiled resources defined within US Core.
More information on US Core can be found [here](https://www.hl7.org/fhir/us/core/). 

Quesitonnaire and QuestionnaireResponses defined within this specification reference terminologies (ValueSets) defined within the Value Set Authoring Center (VSAC). OIDs for the ValueSets referenced from the Questionnaires and QuestionnaireResponses are:
* [NHSNHealthcareServiceLocationCode: 2.16.840.1.113883.13.19](https://vsac.nlm.nih.gov/valueset/2.16.840.1.113883.13.19/expansion/Latest)
* [NHSNPrimaryResidentServiceType: 2.16.840.1.113883.10.20.5.1.5.9.3](https://vsac.nlm.nih.gov/valueset/2.16.840.1.113883.10.20.5.1.5.9.3/expansion/Latest)
* [NHSNSignificantPathogenCode: 2.16.840.1.114222.4.11.3194](https://vsac.nlm.nih.gov/valueset/2.16.840.1.114222.4.11.3194/expansion/Latest)
* [NHSNSpecimenTypeCode: 2.16.840.1.114222.4.11.3249](https://vsac.nlm.nih.gov/valueset/2.16.840.1.114222.4.11.3249/expansion/Latest)



[Next Page - Downloads](downloads.html)