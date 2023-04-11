###### [Archivematica Manual](../README.md) `>` [Processing Configurations](overview.md)

# Processed AIP, open, no DIP
Config name: `prc_opn_noDIP`

Files are normalized for preservation but not access; no DIPs are created or stored.

Use cases:
- Materials where `access status` = "Open, offline access".
- E.g. organization's business records, person's family photos.

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
| Upload DIP: | Do not upload DIP |
| Store DIP? | Do not store |
| Store DIP location: | None |

###### Last updated: Apr 11, 2023
