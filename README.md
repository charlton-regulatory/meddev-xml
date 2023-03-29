# meddev-xml
Support for the xml versions of the MEDDEV 2.12/1 MIR and FSCA reporting forms.

Current versions are:

- MIR v7.2.1b
- FSCA v2.7

Original XML schema files for the MIR have been obtained from
https://www.medical-device-regulation.eu/meddev-guidance-list-download/.

FSCA schema are currently not available on Europa, however these legacy versions have been obtained
and confirmed to support valid XML (see [Known Compatibility](#Known-Compatibility) below).

## Schema Files (XSD)
The XSD schema files are in the schema folder, and there are numerous schema as follows:

For the MIR, there are separate schema for:

- an initial report, using [incident-Initial-v7.2.1](./schema/incident-Initial-v7.2.1.xsd)
- a combined initial and final report, using [incident-InitialFinal-v7.2.1](./schema/incident-InitialFinal-v7.2.1.xsd)
- a follow-up report, using [incident-Followup-v7.2.1](./schema/incident-Followup-v7.2.1.xsd)
- a final, reportable incident report, using [incident-FinalRep-v7.2.1](./schema/incident-FinalRep-v7.2.1.xsd)
- a final, non-reportable incident, using [incident-FinalNonRep-v7.2.1](./schema/incident-FinalNonRep-v7.2.1.xsd)

For the FSCA, there are separate schema for:

- an initial report, using [FSCA_Initial_v2.6](./schema/FSCA_Initial_v2.6.xsd)
- a follow-up report, using [FSCA_Followup_v2.6](./schema/FSCA_Followup_v2.6.xsd)
- a final report, using [FSCA_Final_v2.6](./schema/FSCA_Final_v2.6.xsd)


## Known Compatibility
XML files complying with these templates have been successfully used and submitted to:

- The new MHRA MORE portal
- The BSI eVigilance portal


### Ensuring Compatible XML
One way to ensure your XML is compatible is to export XML from the MIR and FSCA forms available from Europa.
These are always compatible, and the files will validate against the schema and successfully upload to the
above portals.

If you are creating your own XML exports from other tools, then refer to the [XML-FORMAT](XML-FORMAT.md)
guide.


> **PLEASE NOTE:** Consult the current MEDDEV 2.12/1 guidelines and device specific guidance available
> at https://health.ec.europa.eu/system/files/2022-01/md_guidance_meddevs_0.pdf. If submitting in the UK,
> also consult the latest MHRA guidance at https://www.gov.uk/government/collections/medical-devices-guidance-for-manufacturers-on-vigilance.