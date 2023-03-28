###### [Archivematica Manual](../README.md) `>` Processing Configurations

# Processing Configurations
Archivematica `processing configurations` regulate how many `decision points` are exposed to the archivist, requiring them to select among several options for processing. The Archives has structured the standard default `processing config` to minimize the number of `decision points` that require manual intervention. Custom `processing configs` automate ingest by specifying in advance **all** decision point selections for a given transfer. Not all transfers can be handled in the same way, so the Archives has created multiple custom `processing configs` to cover most ingest scenarios.

Standard and custom `processing configs` are (or will be) the same for the Archives' two Archivematica pipelines. Not all configs have yet been created in both pipelines (as of Mar 2023).

## Standard configuration
- [Standard (default) processing config](standard.md)

This is the default standard configuration. It exposes 10 `decision points` that require manual intervention; see [Decision Points](../ingest-guidelines/decisions-points.md) for a description of options.

## Archivematica backlog
| Config | Description |
|:---	   |:---         |
| [bcklog_AM](bcklg-am.md) | Sends transfer to Archivmatica backlog |

This config sends transfer packages to the Archivematica `Backlog` tab.
- Use **only** when you intend to use Archivematica for appraisal, selection and arrangement via the `Appraisal` tab and in the near future.
- Archivematica's `Backlog` space should not be used for long-term backlog storage; create `Backlog AIPs` instead.

## Backlog AIPs
| Config | Description |
|:---	   |:---         |
| [bcklg_encr](bcklg-encr.md) | Full AIP, no normalization, send to encrypted storage |
| [bcklg_opn](bcklg-opn.md) | Full AIP, no normalization, send to open (non-encrypted) storage |

These configs create full Archivematica AIPs, but with **no** normalization for preservation or access, i.e. files are stored in original formats only.

Use to send transfers to backlog for later processing (appraisal, selection, arrangement) outside Archivematica. Later processing entails download, work on the files, then re-ingest of the new package to Archivematica and deletion of the old `Backlog AIP`.

Normalization is omitted at this stage because:
- Preservation copies would be created in the same directory as the originals, making later processing (and re-ingest) more cumbersome – the processing archivist will want to work on the set of original files rather than a double set of originals + preservation copies.
- Access copies would be created and stored to a single directory, regardless of their location in the original folder hierarchy – this makes it difficult to locate access copies as needed.

The main variable here is whether or not to encrypt the `Backlog AIP`.
- Choose to encrypt if there is any possibility that the transfer contains personal or confidential information.

## Processed AIPs
| Config | Description |
|:---	   |:---         |
| [prc_opn_noDIP](prc-opn-nodip.md) | Open storage, no DIP normalization or storage |
| [prc_opn_dipMNL_atm](prc-opn-dipmnl-atm.md) | Open storage, DIP created manually outside Archivematica, send DIP to AtoM |
| [prc_opn_dipMNL_str](prc-opn-dipmnl-str.md) | Open storage, DIP created manually outside Archivematica, do not send DIP to AtoM |
| [prc_opn_dipAM_atm](prc-opn-dipam-atm.md) | Open storage, normalize for access, send DIP to AtoM |
| [prc_opn_dipAM_str](prc-opn-dipam-str.md) | Open storage, normalize for access, do not send DIP to AtoM |
| [prc_encr_noDIP](prc-encr-nodip.md) | Encrypted storage, no DIP normalization or storage |
| [prc_encr_dipMNL_atm](prc-encr-dipmnl-atm.md) | Encrypted storage, DIP (redacted) created manually outside Archivematica, send (redacted) DIP to AtoM |
| [prc_encr_dipMNL_str](prc-encr-dipmnl-str) | Encrypted storage, DIP (redacted) created manually outside Archivematica, do not send DIP to AtoM |
| [prc_encr_dipAM_str](prc-encr-dipam-str.md) | Encrypted storage, normalize for access, do not send DIP to AtoM |

Use these configs for fully processed AIPs, i.e. contents will not require further action or changes. The main variables are whether to:
- Store encrypted or open.
- Create DIPs via Archivematica or manually or not at all.
- Send DIPs to AtoM or not.

Pending review materials should be stored encrypted.

If DIPs are created, they are stored. DIPs for restricted materials may be created by making a redacted copy outside Archivematica; see the [DIP management section](../dip-management/overview.md).

###### Last updated: Mar 28, 2023
