# Definition
In this documentation we will be identifying the migration from legacy systems to MasterPlan.

# Sample Files

[General Ledger](MigrationFiles/GL_Export_by_Date_60M1P.csv)  
[Accounts Payable](MigrationFiles/Accounts_Payable_60M21.csv)  
[Accounts Receivable](MigrationFiles/Accounts_Receivable_60M26.csv)  
[Unit Occupiers](MigrationFiles/List_of_Current_Unit_Occupiers_60M7Q.csv)  
[Unit Owners](MigrationFiles/List_of_Current_Unit_Owners_60M7N.csv)  
[Post Dated Cheque List](MigrationFiles/Post_Dated_Cheque_List_60M3I.csv)  
[Unit Ledger](MigrationFiles/Unit_Ledger_Journals_60M2E.csv)  

# General Ledger
We are representing the project general ledger in the "OA Ledger" under the project ledgers screen.  
Each row in the csv file represents a Journal which is defined in the system at this link: [Journal Definitions](https://github.com/kaizenams/masterplan-web/blob/master/src/app/ledgers/models/journal.model.ts) .  

CSV Column      | Corresponding Journal Field   | Notes 
------          | ------                        | ------
transactiondate | journal_date                  | -
accname         | contact                       | We should map the id from the contact name here
unit            | unit                          | We should map the unit id from the unit name here
invoice         | invoice                       | -
reference       | description                   | -
chequeno        | cheque                        | -
receiptno       | receipt                       | -
transtotal      | debit/credit                  | If number is positive, debit, if negative credit
category        | account                       | There is a map to be applied. Refer to next section
costcenter      | cost_center                   | We should map the id from the cost center in the system
general         | -                             | If this field is populated, target account will be according to the map provided in the "Category to Account Mapping" section
reserve         | -                             | If this field is populated, target account will be reserve fund (Code 12; Refer to the Map File)
subfund         | -                             | Discard this field but show a warning if populated
presenteddate   | posting_date                  | Insert current date
-               | imported                      | Assign true, so in the future we will know, this journal was imported

Other fields of the Journal object will be left empty.

# Category to Account Mapping

[Map File](MigrationFiles/Mollak_Categories.xlsx)

