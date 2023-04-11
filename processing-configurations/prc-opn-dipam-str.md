###### [Archivematica Manual](../README.md) `>` [Processing Configurations](overview.md)

# Processed AIP, open, DIPs created by Archivematica, not sent to AtoM
Config name: `prc_opn_dipAM_str`

Use for materials that will be sent not be sent to AtoM but you want Archivematica to create DIPs for offline access / delivery.
- You must process each archival file as its own AIP in this scenario; otherwise all DIPs will be flattened into a single DIP folder.

Use cases:
- Transfer has a small number of archival files (so ingesting each individual is not onerous) and each has a large number of items of various file formats (so normalizing for access is worthwhile).

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
| Normalize: | Normalize for preservation and access |
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
| Upload DIP: | Do not upload DIP |
| Store DIP? | Store DIP |
| Store DIP location: | <<pipeline>> production DIP store |

###### Last updated: Apr 11, 2023
