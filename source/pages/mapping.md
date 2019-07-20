---
title: Mapping
layout: default
active: other
---

<!-- { :.no_toc } -->

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

<!-- * Do not remove this line (it will not be displayed)
{:toc} -->

<!-- end TOC -->

### Mapping to CDA
  
  <p>NOTE to commenters: BEFORE PUBLICATION this mapping will be updated - it is incomplete now due to the fact that the mappings will likely change during ballot.</p>
  <p>This implementation guide is the first FHIR release of the HAI LCTF reporting profiles and is being balloted in the same cycle as the HL7 CDA® R2 Implementation Guide: NHSN Healthcare Associated Infection (HAI) Long Term Care Facility (LTCF) Reports
Release 1, STU 1—US Realm.</p>
  <p>The following table shows the mapping between FHIR Questionnaire items and the corresponding CDA templates</p>
  <h3><a href="Questionnaire-hai-ltcf-questionnaire-mdro-cdi-event.html">HAI Laboratory Identified MDRO or CDI Event Report for LTCF</a></h3>
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
  
  <h3><a href="Questionnaire-hai-ltcf-questionnaire-mdro-cdi-summary.html">MDRO and CDI LabID Event Reporting Monthly Summary Data for LTCF</a></h3>
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
    
  </table>
