###### [Archivematica Manual](../README.md) `>` [Processing Configurations](overview.md)

# Backlog AIP - Encrypted
Config name: `bcklg_encr`

Use to create a `Backlog AIP` with encrypted storage (i.e. transfer is known to or may contain personal or confidential information).

| Microservice | Setting |
| :---	       |:---     |
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
| Normalize: | Do not normalize |
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
| Store AIP location: | Encrypted AIPs <pipeline1> and <pipeline2> |
| Upload DIP: | Do not upload DIP |
| Store DIP? | Do not store |
| Store DIP location: | None |

###### Last updated: Mar 28, 2023
