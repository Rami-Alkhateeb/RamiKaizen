# Definition

Each budget item is the line-item in the budget study that is entered by the system users.  
Budget item is the rows in each version of the budget. 

# Properties
Budget Item entity doesn't correspond to any collection in the system database, however it is stored as an array under the budget entity's items field.


| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
budget|Int|FK|Budget|The budget item's assigned budget|Auto assigned
account|Int|FK|Account|Assigned account of the budget item|Auto assigned
driver|Int|FK|Budget Driver|Assigned driver of the budget item|Dropdown
amount|Float|-|-|Budgeted amount for the budget item|User entry
details|JSON|-|-|-|Auto generated
version|Int|FK|Budget Version|Assigned version of the budget item|Auto assigned

#Budget Item Details Field Definition

The field “details” in the budget item tuple represents the values and enabled flag of the budget item for the cost center allocation of the budgeted amount.
Please refer to “Editing / Viewing Budgets” section of this document for the visual representation of a budget item on the design. The structure of the details field is as below:
```
{
  cc1:{enabled:bool,amount:float},
  cc2:{enabled:bool,amount:float},
  cc3:{enabled:bool,amount:float},
  …,
  ccn:{enabled:bool,amount:float}
}
```
Each cost center of the project should be represented for each budget item tuple recorded in the database irrespective of if it is enabled or not. 
