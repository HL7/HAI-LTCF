[Previous Page - Acknowledgements](acknowledgements.html)

<!-- { :.no_toc } -->

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

<!-- * Do not remove this line (it will not be displayed)
{:toc} -->

<!-- end TOC -->

### Mapping to CDA
  
  <p>This implementation guide is the first FHIR release of the HAI LCTF reporting profiles and is being balloted in the same cycle as the HL7 CDA® R2 Implementation Guide: NHSN Healthcare Associated Infection (HAI) Long Term Care Facility (LTCF) Reports
Release 1, STU 1—US Realm.</p>
  <p>The following tables show the mapping between FHIR Questionnaire items and the corresponding CDA templates</p>
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


[Next Page - Downloads](downloads.html)