### Overview

This implementation guide (IG) specifies standards for electronic submission of Healthcare Associated Infection (HAI) Long Term Care Facilities (LTCF) reports to the National Healthcare Safety Network (NHSN) of the Centers for Disease Control and Prevention (CDC). This IG contains a library of FHIR profiles for electronic submission of HAI LTCF reports to the NHSN.

As reports are modified and new report types are defined, CDC and Health Level Seven (HL7) will develop and publish additional constraints.

Throughout this process, CDC remains the authority on NHSN data collection protocols. When healthcare enterprises choose to participate in NHSN, they must report to CDC reportable events such as identified MDRO (multidrug-resistant organism) or CDI (C. difficile infection) occurrences such as specific reportable procedures, even those without complications, and events such as a bloodstream infection, either confirmed by a positive blood culture or supported by a patients clinical symptoms. This specification opens the channel for data submission by all applications compliant with the data coding requirements defined here.

Note that participation in the NHSN requires enrollment and filing of reporting plans, which are not defined by this specification. For an overview of NHSN and full information on NHSN participation requirements, see: [http://www.cdc.gov/nhsn](http://www.cdc.gov/nhsn). Provisions of the Public Health Service Act protect all data reported to NHSN from discovery through the Freedom of Information Act (FOIA).


### Relationship to Another Standard

HL7 has developed this FHIR implementation guide in parallel with the CDA implementation guide. We anticipate several STU releases on the path to a Normative Release 1 of the HL7 implementation guides for CDA and FHIR for Healthcare Associated Infection (HAI) Reports from Long Term Care Facilities (LTCF). The FHIR and CDA implementation guides will align. A change to one standard will require the same change in the other standard. 

In this release, the new forms included in both the CDA and FHIR standards are:
* **NHSN HAI LTCF Population Summary Report**: MDRO and CDI LabID Event Reporting Monthly Summary Data for LTCF
* **NHSN HAI LTCF Single-Person Event Report**: Laboratory-identified MDRO or CDI Event for LTCF

For further details see the [NHSN website](https://www.cdc.gov/nhsn/) for reporting healthcare-associated infections in long-term care facilities.


### Audience

The audience for this work is all developers of software systems who want to enable their systems for reporting HAI data to the NHSN.

### Change Notification Process

CDC maintains an e-mail list of contacts at organizations interested in or responsible for implementations of FHIR for LTCF HAI reporting to NHSN. To be added to the list, send a request with your contact information to nhsncda@cdc.gov. CDC uses the list for e-mail notifications of changes, including new data requirements. Changes may apply to this IG and to other documents such as business rules that are needed to implement and support FHIR for LTCF HAI reporting to NHSN. NHSN CDA related information may be found at https://www.cdc.gov/nhsn/cdaportal/index.html.  

### Acknowledgements

This implementation guide was produced and developed by Lantana Consulting Group in conjunction with the Division of Healthcare Quality Promotion in the National Center for Emerging and Zoonotic Infectious Diseases (NCEZID) at the Centers for Disease Control and Prevention (CDC). Its development and deployment are results of the dedication of the team—led by Daniel A. Pollock, M.D., Surveillance Branch Chief, Division of Healthcare Quality Promotion, NCEZID, CDC and  Jeneita Bell, MD, MPH, Long-term Care Team Lead, DHQP, NCEZID, CDC—and their support of the development of interoperable data standards for the CDC’s National Healthcare Safety Network (NHSN).  

Special thanks and acknowledgment to stakeholders who participated in calls and provided feedback. Specifically, we would like to thank  Cindy Frakes, Steve Herron, Jamie Gatzke, Kelly Luden, Prasath Govindarajulu from Cerner;  Laura Ditz, Nancy Chi, Nichole (Nicki) Fetterman, Michael Furman, Patti Barton, Aga Lee from Point Click Care; Donna Doneski from NASL; and  Denise Wassenaar, Doc DeVore, Rob Price from Matrix  Care. 

The best standards are those driven by business requirements. A strong set of Healthcare Associated Infection (HAI) surveillance application vendors monitor, evaluate, and test each release of this guide.  


|-----|-----|-----|-----| 

|Primary Editor:|Sarah Gaunt|Lantana Consulting Group|sarah.gaunt@lantanagroup.com| 
|Primary Editor:|Zabrina Gonzaga|Lantana Consulting Group|zabrina.gonzaga@lantanagroup.com| 
|Primary Editor:|Dave deRoode|Lantana Consulting Group|david.deroode@lantanagroup.com| 
|Co-Editor:|Jeneita Bell, MD, MPH|CDC|hpq8@cdc.gov| 
|Co-Editor:|Angella Antilla PhD, MSN|CDC|vtb9@cdc.gov| 
|Co-Editor:|Daniel Pollock, M.D.|CDC|DPollock@cdc.gov| 
|Co-Editor:|Ahmed Tahir|Leidos Consultant to CDC/NHSN|nmn8@cdc.gov| 
|Co-Editor:|Mindy Durrance|Leidos Consultant to CDC/NHSN|mdq1@cdc.gov| 
|Co-Editor:|Sheri Chernetsky Tejedor, MD|CDC|yei9@cdc.gov| 
|Co-Editor:|Sheila Abner|CDC|sha8@cdc.gov| 
|Co-Chair:|Erin Holt MPH|Tennessee Department of Health|erin.holt@tn.gov| 
|Co-Chair:|Laura Rappleye|Altarum|laura.rappleye@altarum.org| 
|Co-Chair:|Craig Newman|Altarum|craig.newman@altarum.org| 
|Co-Chair:|Danny Wise|Allscripts|danny.wise@allscripts.com| 
|Co-Chair:|Joginder Madra|Madra Consulting Inc.|hl7@madraconsulting.com| 
|Co-Chair:|Gaye Dolin M.S.N., R.N. |Intelligent Medical Objects |gdolin@imo-online.com| 
|Co-Chair:|Calvin Beebe|Mayo Clinic|cbeebe@mayo.edu| 
|Co-Chair:|Austin Kreisler|Leidos Consultant to CDC/NHSN|duz1@cdc.gov| 
|Co-Chair:|Andrew Statler|Cerner Corp|andrew.statler@cerner.com| 
|Co-Chair:|Sean McIlvenna| Lantana Consulting Group|sean.mcilvenna@lantanagroup.com| 
|Co-Chair:|Benjamin Flessner|Redox|benjamin@redoxengine.com| 
|Co-Editor:|Beau Bannerman|Lantana Consulting Group|beau.bannerman@lantanagroup.com| 
|Technical Editor:|Diana Wright|Lantana Consulting Group|diana.wright@lantanagroup.com| 
|Technical Editor:|Chris Hannigan|Lantana Consulting Group|chris.hannigan@lantanagroup.com| 




### Authors

<table>
<thead>
<tr>
<th>Name</th>
<th>Email/URL</th>
</tr>
</thead>
<tbody>
<tr>
<td>HL7 International - Public Health Work Group</td>
<td><a href="http://www.hl7.org/Special/committees/pher/" target="_new">http://www.hl7.org/Special/committees/pher/</a></td>
</tr>
</tbody>
</table>


