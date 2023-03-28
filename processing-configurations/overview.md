###### [Archivematica Manual](../README.md) `>` Processing Configurations

# Processing Configurations
Archivematica `processing configurations` regulate how many `decision points` are exposed to the archivist, requiring them to select among several options for processing. The Archives has structured the standard default `processing config` to minimize the number of `decision points` that require manual intervention. Custom `processing configs` automate ingest by specifying in advance **all** decision point selections for a given transfer. Not all transfers can be handled in the same way, so the Archives has created multiple custom `processing configs` to cover most ingest scenarios.

Standard and custom `processing configs` are (or will be) the same for the Archives' two Archivematica pipelines. Not all configs have yet been created in both pipelines (as of Mar 2023).

## Standard configuration
- [Standard (default) processing config](standard.md)

This is the default standard configuration. It exposes 10 `decision points` that require manual intervention; see [Decision Points](../ingest-guidelines/decisions-points.md) for a description of options.

## Archivematica backlog
| [bcklog_AM](bcklg-am.md) | Sends transfer to Archivmatica backlog |

This config sends transfer packages to the Archivematica `Backlog` tab.
- Use **only** when you intend to use Archivematica for appraisal, selection and arrangement via the `Appraisal` tab and in the near future.
- Archivematica's `Backlog` space should not be used for long-term backlog storage; create `Backlog AIPs` instead.

## Backlog AIPs
- [bcklg_opn](bcklg-opn.md) – open
- [bcklg_encr])(bcklg-encr.md) – encrypted

These configs create full Archivematica AIPs, but with **no** normalization for preservation or access, i.e. files stored in original formats only.
- Use to send transfers to backlog for later processing (appraisal, selection, arrangement) outside Archivematica.

Later processing entails re-ingest of the new package to Archivematica and deletion of the old `Backlog AIP`. Normalization is omitted at this stage because:
- Preservation copies would be created in the same directory as the originals, making later processing (and re-ingest) more cumbersome (the processing archivist will want to work on the set of original files rather than a double set of originals + preservation copies).
- Access copies would be created and stored to a single directory, regardless of their location in the original folder hierarchy, making it difficult to locate access copies as needed.

The main variable here is whether or not to encrypt the `Backlog AIP`.
- Choose to encrypt if there is any possibility that the transfer contains personal or s

Config:
## Processed AIPs


---
###### Last updated: Jan 26, 2022
