### LTCF HAI Reporting Background

LTCF HAI reporting standards were first released in 2012, with data submitted to NHSN by paper form and manual web entry. The CDA and FHIR standards for electronic HAI reporting from LTCFs were balloted for the first time in 2019. This FHIR IG, and its parallel CDA IG, permit LTCFs to submit standardized surveillance data for public reporting of HAI and other reportable events to NHSN directly from electronic health record (EHR) systems. This method of data collection and submission to NHSN can greatly reduce reporter burden and improve work efficiency. It is also expected that data errors may decrease, thereby improving data quality for national benchmarks, monitoring trends, and measuring progress towards infection prevention goals. Going forward, as this IG will likely be updated and expanded every year, it will continue to go through the HL7 ballot comment and reconciliation process each time. 

### Current Release

This IG is the first STU release of the LTCF HAI reporting templates. It specifies the creation of two reports : 

NHSN HAI LTCF Population Summary Report: MDRO and CDI LabID Event Reporting Monthly Summary Data for LTCF 

NHSN HAI LTCF Single-Person Event Report: Laboratory-identified MDRO or CDI Event for LTCF 

Please note, the latest NHSN Long-Term Care Facility Component modifications published will apply to events on or after January 1, 2020 (See: CDC/NHSN Long-Term Care Facility (LTCF) Component Summary of Modifications, January 2020. https://www.cdc.gov/nhsn/pdfs/ltc/ltcf-summary-of-changes_current.pdf). Future work on LTCF HAI reporting will continue to expand the set of forms covered by the standard. 

For further details see the [NHSN website](https://www.cdc.gov/nhsn/) for reporting healthcare-associated infections in long-term care facilities. 

 

### Mapping to CDA

This implementation guide is the first FHIR release of the HAI LCTF reporting profiles and is being balloted in the same cycle as the HL7 CDA® R2 Implementation Guide: NHSN Healthcare Associated Infection (HAI) Long Term Care Facility (LTCF) Reports Release 1, STU 1—US Realm.

The following tables show the mapping between FHIR Questionnaire items and the corresponding CDA templates

 [HAI Laboratory Identified MDRO or CDI Event Report for LTCF](Questionnaire-hai-ltcf-questionnaire-mdro-cdi-event.html)

  <table class="codes"> 

    <thead> 

      <tr> 

        <td> 

          <b>FHIR Questionnaire Item</b> 

        </td> 

        <td> 

          <b>FHIR Questionnaire Item linkId</b> 

        </td> 

        <td> 

          <b>CDA Mapping</b> 

        </td> 

      </tr> 

    </thead> 

    <tbody> 

      <tr> 

        <td>Facility ID</td> 

        <td>facility</td> 

        <td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/id</td> 

      </tr> 

      <tr> 

        <td>Resident Id</td> 

        <td>US Core Patient.identifier</td> 

        <td>ClinicalDocument/recordTarget/patientRole/id</td> 

      </tr> 

      <tr> 

        <td>Social Security #</td> 

        <td>US Core Patient.identifier</td> 

        <td>ClinicalDocument/recordTarget/patientRole/id</td> 

      </tr> 

      <tr> 

        <td>Medicare #</td> 

        <td>US Core Patient.identifier</td> 

        <td>ClinicalDocument/recordTarget/patientRole/id</td> 

      </tr> 

      <tr> 

        <td>Resident name: Last</td> 

        <td>US Core Patient.name.family</td> 

        <td>ClinicalDocument/recordTarget/name</td> 

      </tr> 

      <tr> 

        <td>Resident name: First</td> 

        <td>US Core Patient.name.given</td> 

        <td>ClinicalDocument/recordTarget/name</td> 

      </tr> 

      <tr> 

        <td>Resident name: Middle</td> 

        <td>US Core Patient.name.given</td> 

        <td>ClinicalDocument/recordTarget/name</td> 

      </tr> 

      <tr> 

        <td>Gender</td> 

        <td>US Core Patient.gender</td> 

        <td>ClinicalDocument/recordTarget/patientRole/patient/administrativeGenderCode</td> 

      </tr> 

      <tr> 

        <td>Date of Birth</td> 

        <td>US Core Patient.birthDate</td> 

        <td>ClinicalDocument/recordTarget/patientRole/patient/birthTime</td> 

      </tr> 

      <tr> 

        <td>Ethnicity</td> 

        <td>US Core Patient.us-core-ethnicity</td> 

        <td>ClinicalDocument/recordTarget/patientRole/patient/ethnicGroupCode</td> 

      </tr> 

      <tr> 

        <td>Race</td> 

        <td>US Core Patient.us-core-race</td> 

        <td>ClinicalDocument/recordTarget/patientRole/patient/raceCode</td> 

      </tr> 

      <tr> 

        <td>Date First Admitted to Facility</td> 

        <td>date-of-first-admission-to-facility</td> 

        <td>First Admission Encounter in a Lab Identified Report LTCF/effectiveTime/low</td> 

      </tr> 

      <tr> 

        <td>Date of Current Admission to Facility</td> 

        <td>date-of-current-admission-to-facility</td> 

        <td>ClinicalDocument/componentOf/encompassingEncounter/effectiveTime/low</td> 

      </tr> 

      <tr> 

        <td>Date Specimen Collected</td> 

        <td>date-specimen-collected</td> 

        <td>Specimen Collection Procedure in a Lab Identified Report LTCF/effectiveTime/low</td> 

      </tr> 

      <tr> 

        <td>Specimen Type</td> 

        <td>specimen-type</td> 

        <td>Specimen Collection Procedure in a Lab Identified Report LTCF/participant/participantRole/playingEntity/code</td> 

      </tr> 

      <tr> 

        <td>Specific Organism Type</td> 

        <td>specific-organism-type</td> 

        <td>Pathogen Identified Organism in a Lab Identified Report LTCF/value</td> 

      </tr> 

      <tr> 

        <td>Resident Care Location</td> 

        <td>resident-care-location</td> 

        <td>ClinicalDocument/componentOf/encompassingEncounter/location/healthcareFacility/id/@extension</td> 

      </tr> 

      <tr> 

        <td>Primary Resident Service Type</td> 

        <td>primary-resident-service-type</td> 

        <td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/code</td> 

      </tr> 

      <tr> 

        <td>Has resident been transferred from acute care facility in past 4 weeks?</td> 

        <td>transfer-from-acute-care-facility</td> 

        <td>Transfer from an Acute Care Facility to LTCF in a Lab Identified Report/value</td> 

      </tr> 

      <tr> 

        <td>Date of transfer from acute care to your facility</td> 

        <td>date-of-last-transfer</td> 

        <td>Transfer from an Acute Care Facility to LTCF in a Lab Identified Report/effectiveTime</td> 

      </tr> 

      <tr> 

        <td>Was resident on antibiotic therapy for this organism type at the time of transfer to your facility</td> 

        <td>antibiotic-at-time-of-transfer</td> 

        <td>Antibiotic Treatment at time of Transfer in a Lab Identified Report LTCF/value</td> 

      </tr> 

      <tr> 

        <td>NHSN Comment</td> 

        <td>nhsn-comment</td> 

        <td>NHSN Comment Section/NHSN Comment</td> 

      </tr> 

    </tbody> 

  </table> 

   

[MDRO and CDI LabID Event Reporting Monthly Summary Data for LTCF](Questionnaire-hai-ltcf-questionnaire-mdro-cdi-summary.html)

<table class="codes"> 

  <thead> 

    <tr> 

      <td> 

        <b>FHIR Questionnaire Item</b> 

      </td> 

      <td> 

        <b>FHIR Questionnaire Item linkId</b> 

      </td> 

      <td> 

        <b>CDA Mapping</b> 

      </td> 

    </tr> 

  </thead> 

  <tbody> 

    <tr> 

      <td>Facility ID</td> 

      <td>facility</td> 

      <td>ClinicalDocument/participant/associatedEntity/id/@root</td> 

    </tr> 

    <tr> 

      <td>First Day of Period Reported</td> 

      <td>report-period-start</td> 

      <td>ClinicalDocument/documentationOf/serviceEvent/effectiveTime/low</td> 

    </tr> 

    <tr> 

      <td>Last Day of Period Reported</td> 

      <td>report-period-end</td> 

      <td>ClinicalDocument/documentationOf/serviceEvent/effectiveTime/high</td> 

    </tr> 

    <tr> 

      <td>Facility Location Code</td> 

      <td>facility-location-code</td> 

      <td>ClinicalDocument/participant/associatedEntity/id/@extension</td> 

    </tr> 

    <tr> 

      <td>Resident Days</td> 

      <td>resident-days</td> 

      <td>Summary Data Observation LTCF[code/@code="1369-8']/value</td> 

    </tr> 

    <tr> 

      <td>Resident Admissions</td> 

      <td>resident-admissions</td> 

      <td>Summary Data Observation LTCF[code/@code="1370-6']/value</td> 

    </tr> 

    <tr> 

      <td>Number of Admissions on C. diff Treatment</td> 

      <td>number-admissions-on-c-diff-treatment</td> 

      <td>Summary Data Observation LTCF[code/@code="1371-4']/value</td> 

    </tr> 

    <tr> 

      <td>Number of C. diff Treatment Starts</td> 

      <td>number-c-diff-treatment-starts</td> 

      <td>Summary Data Observation LTCF[code/@code="1372-2']/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - Methicillin-resistant Staphylococcus aureus</td> 

      <td>no-lab-id-event-mrsa</td> 

      <td>Report No Events[code/@code="3030-4"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - Methicillin-sensitive Staphylococcus aureus</td> 

      <td>no-lab-id-event-mssa</td> 

      <td>Report No Events[code/@code="1307-8"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - Vancomycin resistant Enterococcus</td> 

      <td>no-lab-id-event-vre</td> 

      <td>Report No Events[code/@code="3033-8"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - CephR Klebsiella</td> 

      <td>no-lab-id-event-cephr-klebsiella</td> 

      <td>Report No Events[code/@code="3036-1"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - CRE E. coli</td> 

      <td>no-lab-id-event-mrsa-cre-e-coli</td> 

      <td>Report No Events[code/@code="3039-5"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - CRE Enterobacter</td> 

      <td>no-lab-id-event-mrsa-cre-enterobacter</td> 

      <td>Report No Events[code/@code="3042-9"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - CRE Klebsiella</td> 

      <td>no-lab-id-event-cre-klebsiella</td> 

      <td>Report No Events[code/@code="3045-2"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - Acinetobacter</td> 

      <td>no-lab-id-event-mdr-acinetobacter</td> 

      <td>Report No Events[code/@code="3048-6"]/value</td> 

    </tr> 

    <tr> 

      <td>Report no labID event - All specimens - Clostridium difficile</td> 

      <td>no-lab-id-event-c-difficile</td> 

      <td>Report No Events[code/@code="3051-0"]/value</td> 

    </tr> 

  </tbody> 

</table> 

 

### References

| Name | Description | 

|------|-------------| 

| [HL7 CDA® R2 Implementation Guide: National Healthcare Safety Network (NHSN) Healthcare Associated Infection (HAI) Reports for Long Term Care Facilities (HAI-LTCF-CDA), Release 1- US Realm](http://www.hl7.org/special/Committees/projman/searchableProjectIndex.cfm?action=edit&ProjectNumber=1511)    | This project developed an implementation guide constraining CDA Release 2. The implementation guide supports electronic submission of HAI LTCF data to the National Healthcare Safety Network.| 

| [HL7 FHIR® Implementation Guide: Healthcare Associated Infection Reports, Release 1 - US Realm](http://hl7.org/fhir/us/hai/index.html)| This implementation guide (IG) is to specifies standards for electronic submission of Healthcare Associated Infection (HAI) reports to the National Healthcare Safety Network (NHSN) of the Centers for Disease Control and Prevention (CDC). This IG contains a library of FHIR profiles for electronic submission of HAI reports to the NHSN. | 

| [US Core Implementation Guide (v3.0.0)](http://hl7.org/fhir/us/core/index.html)    | The US Core Implementation Guide is based on [FHIR Version 4.0.0](http://hl7.org/fhir/R4/index.html) and defines the minimum conformance requirements for accessing patient data The Argonaut pilot implementations, [ONC 2015 Edition Common Clinical Data Set (CCDS)](https://www.healthit.gov/sites/default/files/ccds_reference_document_v1_1.pdf) and the latest proposed [ONC U.S. Core Data for Interoperability (USCDI)](https://www.healthit.gov/topic/laws-regulation-and-policy/notice-proposed-rulemaking-improve-interoperability-health) provided the requirements for this guide. These profiles are the foundation for future US Realm FHIR implementation guides. In addition to Argonaut, they are used by [DAF-Research](http://hl7.org/fhir/us/daf-research/index.html), [QI-Core](http://hl7.org/fhir/us/qicore/), and [CIMI](https://www.hl7.org/Special/Committees/cimi/overview.cfm). Under the guidance of HL7 and the HL7 US Realm Steering Committee, the content will expand in future versions to meet the needs specific to the US Realm.| 