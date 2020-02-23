# 2019 Report by the AEA Data Editor
This is the report for 2019. 

## Locations
The repository at [https://github.com/AEADataEditor/report-aea-data-editor-2019-final](https://github.com/AEADataEditor/report-aea-data-editor-2019-final) contains text, code, data, and output from running the code. 

The deposit at [https://doi.org/10.3886/E117884V1](https://doi.org/10.3886/E117884V1) contains code and data, as well as output. 

## Citing the code and data

> Vilhuber, Lars, David Wasser, and James Tu-ritto.2020. “Code and Data for:  Report for2019  by  the  AEA  Data  Editor.”  AmericanEconomic  Association  [publisher],https://doi.org/10.3886/E117884V1

## External dependencies

Two data sources are internal files, not otherwise made available. 

Two data sources are:

> Vilhuber,Lars. 2020a.    “Data    files    for AEA Repository migration.”American Economic Association [publisher],https://doi.org/10.3886/E117873V1.

> Vilhuber,  Lars. 2020b.  “Process  data  for  the AEA  Pre-publication  Verification  Service.” American Economic Association [publisher], https://doi.org/10.3886/E117876V1

## Running code

See the `programs/README.md` file for further details.

## Structure

### Data

Some data needs to be downloaded before being able to run programs; other data is provided within this repository:

#### List of Lab members

```
data/replicationlab_members.txt
```

Listed in the article appendix.

#### Data for pre-production verification

See `data/jira/anon/README.md` for more details. 
Source: Vilhuber (2020b)

```
data/jira/anon/jira.anon.RDS
data/jira/anon/jira.anon.csv
data/jira/anon/README.md
```

#### Data on repository migration

See `programs/README.md` file for further details.
Source: Vilhuber(2020a)

#### Data on RCT registry

These data are provided as part of this repository. For more details, see `programs/README.md`.

```
data/rct/generated
data/rct/generated/AEAcharts.RData
data/rct/generated/aeareg_data.csv
data/rct/generated/reg_data_q3.Rdata
data/rct/generated/regdatedf.Rdata
data/rct/generated/table_preanalysisplans.csv
data/rct/generated/table_preregistrations.csv
data/rct/raw
data/rct/raw/README.md
```

### Programs

All programs are in the `programs` subdirectory:
```
programs/01_prepare-rct.R
programs/02_analysis-rct.R
programs/03_copy_migration_figures.R
programs/04_jira_anonymize.R
programs/05_jira_stats_graphs.R
programs/06_copy_migration_tables.R
programs/07_print_migration_tables.R
programs/README.md
programs/config.R
programs/run_all.sh
```
See the `programs/README.md` file for further details.

### Figures and Images
All images, whether hand-created or generated, are in the `images` directory:

```
images/author_response_hist.png
images/figure_migration_doi_by_year.png
images/figure_migration_files.png
images/figure_migration_software_pkgs.png
images/figure_migration_software_years_pct.png
images/figure_preanalysisplans.png
images/figure_preregistrations.png
images/figure_rctgrowth.png
images/n_assessments_journal_plot.png
images/n_rounds_plot.png
images/revision_round_length_hist.png
images/total_length_hist.png
images/Screenshot_aer_data_citation.png
```

To map these to the relevant figures in the article, see `programs/README.md`  for further details.

## Technical notes (apply only to the Github version)

The repository references at least one external git repo. So do

```
git submodule update --init --recursive
```

after cloning it.

