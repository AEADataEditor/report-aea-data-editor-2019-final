Processing Figures and Tables
=============================
The programs in this folder create the figures and tables in the article. They need to be run before compiling the LaTeX. No post-processing should be needed.

Data sources
------------
- `data/jira`: 
   - `confidential`: Internal data from the JIRA system used by the AEA Data Editor. Not provided.
   - `anon`: Anonymized subset of the internal data used to generate all figures and tables. Download data from Vilhuber(2020c) and save into this folder. `04_jira_anonymize.R` was used to anonymize these data.
- `data/rct`
   - `raw`: Raw data as downloaded from the internal systems at the AEA RCT Registry by James Turitto. Since providing this data, the AEA RCT Registry now provides snapshots of the data at [https://dataverse.harvard.edu/dataverse/aearegistry](https://dataverse.harvard.edu/dataverse/aearegistry). The data here would be similar to AEA RCT Registry(2020), though that has not been verified.
   - `generated`: Simplified data, based on the raw data. Provided as part of this archive. Created by `01_prepare-rct.R`. 
- `externals/aea-supplement-migration/`: Data and Figures from Vilhuber (2020b) and https://github.com/AEADataEditor/aea-supplement-migration. 
   - `programs/`: Source for figures copied to and provided as part of the `images` directory in this repository. Copied using `03_copy_migration_figures.R`
   - `data/generated/`: Source for tables, copied using `06_copy_migration_tables.R` and provided as part of this repository. 
- `tables`: This directory contains data copied using `06_copy_migration_tables.R` and serves as an input to processing in `07_print_migration_tables.R`

Pre-requisites
--------------
- R (last run with 3.6.1)
  - Package `here` is required
  - all other packages are listed at the top of each R program, and will be installed automatically
- Bash shell (optional)
  - used to run all R scripts in sequence

Processing
----------

- run `run_all.sh` from a shell to process all files in numerical order
- Note that in the absence of the raw (confidential) data files used in `01_prepare-rct.R` and `04_jira_anonymize.R`, those step will be skipped. This is normal.

Outputs
-------
Output folders are listed in `config.R`. By default, 
 - figures are in the `(BASEPATH)/images` folder
 - tables (and CSV files) are in the `(BASEPATH)/tables` folder

References
----------
AEA RCT Registry. 2020. “Registrations   in   the   AEA   RCT   Registry   (2013-04 to 2020-01).” Harvard Dataverse UNF:6:kWiM5wm1x75KKsxWAAqr4g==, https://doi.org/10.7910/DVN/DFMLIU.

Vilhuber, Lars. 2020b. "Data and code for:Data files for AEA Repository migration" American Economic Association [publisher], Inter-university Consortium for Political and Social Research [distributor]. http://doi.org/10.3886/E117873V1

Vilhuber,  Lars. 2020c.  “Process  data  for  the AEA  Pre-publication  Verification  Service.” American Economic Association [publisher],https://doi.org/10.3886/E117876V1.


| figure_migration_files.png | | | 
| figure_migration_doi_by_year.png | | | 
| figure_migration_software_pkgs.png | | | 
| figure_migration_software_years_pct.png | | | 
| n_assessments_journal_plot.png | | | 
| n_rounds_plot.png | | | 
| revision_round_length_hist.png | | | 
| total_length_hist.png | | | 
| author_response_hist.png | | | 
| figure_rctgrowth.png | | | 
| figure_preregistrations.png | | | 
| figure_preanalysisplans.png | | | 
