###### [Archivematica Manual](../README.md) `>` [Processing Configurations](overview.md)

# Processed AIP, open, DIPs created manually, sent to AtoM
Config name: `prc_opn_dipMNL_atm`

Use for materials that have access copies created outside Archivematica and can be sent to AtoM from Archivematica.
- Parent descripion (archival file) must already exist in AtoM.
- Ingest folder must be structured with `access` folder containing manually normalized DIPs that have the exact same name as originals (extensions can be different).
- AtoM item-level records will be created for each object in the DIP.
- You must specify the AtoM stub of the existing parent description on the Transfer tab in the `Access system ID` field.

Use cases:
- Original pdfs are very large and you want to manually create smaller access copies in Acrobat using "Save as reduced size".


| Microservice | Setting |
|:---	         |:---     |
| Scan for viruses? | Yes |
| Assign UUIDs to directories? | Yes |
| Generate transfer structure report: | Yes |
| Perform file format identification (Transfer): | Yes |
| Extract packages? | Yes |
| Delete package after extraction? | Yes |
| Perform policy checks on originals? | No |
| Examine contents? | Examine contents |
| Create SIP(s): | Create single SIP and continue processing |
| Perform file format identification (Ingest): | No, use existing data |
| Normalize: | Normalize for preservation |
| Approve normalization: | Yes |
| Choose thumbnail mode: | Yes |
| Perform policy checks on preservation derivatives? | No |
| Perform policy checks on access derivatives? | No |
| Bind PIDs? | No |
| Document empty directories? | Yes |
| Reminder: add metadata if desired: | Continue |
| Transcribe SIP contents? | Yes |
| Perform file format identification (Submission documentation & metadata): | Yes |
| Select compression algorithm: | 7z without compression |
| Select compression level: | 1 - fastest compression |
| Store AIP: | Yes |
| Store AIP location: | <<pipeline>> produciton AIP store |
| Upload DIP: | Upload DIP to AtoM/Binder |
| Store DIP? | Store DIP |
| Store DIP location: | <<pipeline>> production DIP store |

###### Last updated: Apr 11, 2023
