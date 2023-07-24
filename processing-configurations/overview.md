###### [Archivematica Manual](../README.md) `>` Processing Configurations

# Processing Configurations
Archivematica **processing configurations** set default values for **decision point** fields and how many are exposed to the archivist, requiring manual intervention (selection of an option). The Archives has three main types of processing configs:
1. [The Default configuration](default-config.md) - used as default when user clicks the `Start transfer` button rather than selecting a specific config.
1. [Standardized configurations](standardized-configs.md) - 12 configs that cover various common ingest scenarios.
1. [Customized configurations](customized-configs.md) - one-off configs for specific projects.

For more detail, see Archivematica's own [documentation describing processing configuration fields and their options](https://www.archivematica.org/en/docs/archivematica-1.14/user-manual/administer/dashboard-admin/#dashboard-processing).

## Comparison
The table below lists the Archives' processing configs, with links to the settings of each. A comparison table showing settings can also be [downloaded as a spreadsheet here](../downloads/processing-configs-compared.xlsx).

| Config | Description |
|:---	   |:---         |
| [Default](default-config.md) | Default config, exposes 10 decisions point for manual intervention |
| [bcklog_AM](bcklg-am.md) | Sends transfer to Archivmatica backlog |
| [bcklg_encr](bcklg-encr.md) | Full (backlog) AIP, no normalization, send to encrypted storage |
| [bcklg_opn](bcklg-opn.md) | Full (backlog) AIP, no normalization, send to open (non-encrypted) storage |
| [prc_opn_noDIP](prc-opn-nodip.md) | Open storage, no DIP normalization or storage |
| [prc_opn_dipMNL_atm](prc-opn-dipmnl-atm.md) | Open storage, DIP created manually outside Archivematica, send DIP to AtoM |
| [prc_opn_dipMNL_str](prc-opn-dipmnl-str.md) | Open storage, DIP created manually outside Archivematica, do not send DIP to AtoM |
| [prc_opn_dipAM_atm](prc-opn-dipam-atm.md) | Open storage, normalize for access, send DIP to AtoM |
| [prc_opn_dipAM_str](prc-opn-dipam-str.md) | Open storage, normalize for access, do not send DIP to AtoM |
| [prc_encr_noDIP](prc-encr-nodip.md) | Encrypted storage, no DIP normalization or storage |
| [prc_encr_dipMNL_atm](prc-encr-dipmnl-atm.md) | Encrypted storage, DIP (redacted) created manually outside Archivematica, send (redacted) DIP to AtoM |
| [prc_encr_dipMNL_str](prc-encr-dipmnl-str.md) | Encrypted storage, DIP (redacted) created manually outside Archivematica, do not send DIP to AtoM |
| [prc_encr_dipAM_str](prc-encr-dipmnl-str.md) | Encrypted storage, normalize for access, do not send DIP to AtoM |

###### Last updated: Jul 21, 2023
