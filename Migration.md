# Definition
In this documentation we will be identifying the migration from legacy systems to MasterPlan.

# Sample Files

[General Ledger](MigrationFiles/GL_Export_by_Date_60M1P.csv)
[Accounts Payable](Accounts_Payable_60M21.csv)
[Accounts Receivable](Accounts_Receivable_60M26.csv)
[Unit Occupiers](List_of_Current_Unit_Occupiers_60M7Q.csv)
[Unit Owners](List_of_Current_Unit_Owners_60M7N.csv)
[Post Dated Cheque List](Post_Dated_Cheque_List_60M3I.csv)
[Unit Ledger](Unit_Ledger_Journals_60M2E.csv)

# General Ledger
We are representing the project general ledger in the "OA Ledger" under the project ledgers screen.  
Each row in the csv file represents a Journal which is defined in the system at this link: [Journal Definitions](https://github.com/kaizenams/masterplan-web/blob/master/src/app/ledgers/models/journal.model.ts) .  

