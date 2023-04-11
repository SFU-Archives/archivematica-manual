###### [Archivematica Manual](../README.md) `>` [Processing Configurations](overview.md)

# Processed AIP, encrypted, DIPs created manually, sent to AtoM
Config name: `prc_encr_dipMNL_atm`

Use for materials with redacted access copies made outside Archivematica.

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
| Store AIP location: | Encrypted AIPs <<pipelines>> |
| Upload DIP: | Upload DIP to AtoM/Binder |
| Store DIP? | Store DIP |
| Store DIP location: | <<pipeline>> production DIP store |

###### Last updated: Apr 11, 2023
