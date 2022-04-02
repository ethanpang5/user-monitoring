# Spring 2022 Public Editor User Monitoring

production tasks:
- make sure everyone downloads 
- [high] push the covid sources data hunt, iaa, gold standard, and schema files to evidence_eric
- [high] un-hardcode all the cases in insert_into_table():
    - insert into ucs: 
        - data validation [ignore for now]
        - iterate over rows in df (dataframe containing uuid’s and scores) and add them to the the ucs table
    - insert into task_scores:
        - data validation [ignore for now]
        - iterate over rows in df (calculated_task_scores) and add them to the task_scores table
    - insert into datahunt_tracker:
        - data validation [ignore for now]
        - add datahunt id (quiz_task_uuid) as well as num_rows_processed
- [high] ask Nick to create csv’s for the people in each task instead of xlsx going forward
- [high] whitelist all the users in Covid_Source_Users.xlsx
    - at the end of the day we want to keep all of the users in this spreadsheet and associate their uiid’s with their nicknames
    - end up having a table containing nickname, uuid, and ucs score, in descending order
- [medium] figure out way to automate schema reading and loading
- [medium] create functionality to update values in any table in the database:
- [low] figure out way to pull gold standard data when applicable
- [low] data validation capabilities for inert_into_table() and all of its cases
- [low] debug the display helper function in the handler functions cell:
    - we want to be able to print the contents of any table onto the jupyter notebook
- [low] handler function to clear / reset the database tables

demonstration tasks:
- run the pipeline one time starting with Covid_SourceRelevancev1-2022-04-01T0047-DataHunt.csv.gz [quoted source annotation module]
- eventually run the pipeline and save results for each of the different annotation modules
- 
