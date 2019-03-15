# Server initialisation instructions
```mcmd
add group mosaic
give MOSAIC_VIEWER write sys_FileMeta
give MOSAIC_VIEWER write sys_job_ScriptJobExecution
give MOSAIC_VIEWER read sys_scr_Script
give MOSAIC_VIEWER read sys_App
import --from-path ~/git/molgenis-app-mosaic-calculator/molgenis-data-model/mosaic_model.xlsx
import --from-path ~/git/molgenis-app-mosaic-calculator/molgenis-data-model/mosaic_scripts.xlsx
enable rls mosaic_exp_data
give MOSAIC_VIEWER write mosaic_exp_data
# upload mosaic-app zipfile and put it in the menu
give MOSAIC_VIEWER view app-molgenis-app-mosaic-calculator
# Make both file attributes cascade delete in exp_data
add user demo
# Make role USER extend MOSAIC_VIEWER
# If mail works: enable user signup and disable moderation
```