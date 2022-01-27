###### [Archivematica Manual](../README.md) `|` [Ingest Guidelines](overview.md)

# Decision Points
Some Archivematica microservices allow multiple options requiring choice.
- Options can be pre-selected in an automated [custom processing configuration](../processing-configurations/overview.md).
- `Decisions points` occur when microservices settings are **not** pre-configured and therefore require the archivist to manually select an option.

This page describes the `decision points` in the [standard processing configuration](../processing-configurations/standard.md).

## Transfer tab
There is only one `decision point` required on the `Transfer` tab. Pre-defined settings include:
- Generate tree directory structure of the transfer.
- Identify file formats.
- Run BulkExtractor to identify potentially sensitive data (e.g. credit card numbers).

### Create SIP from Transfer
`Create single SIP and continue processing`
- Send transfer to the `Ingest` tab to continue.
- Use if the transfer does not require any additional appraisal, selection, or arrangement.
- Use if it does require addtional processing but you will not be doing this in the immediate future (process through Archivematica to create a `backlog AIP`).

`Send to backlog`
- Send to Archivematica backlog.
- Use this option if you intend to process the transfer in the immediate future (appraise, select, arrange and describe).

`Reject transfer`
- Cancel the ingest process.
- Use if you realize you have a made a mistake and wish to start over.

## Ingest tab


---
###### Last updated: Jan 26, 2022
