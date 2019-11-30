# Definition

Budget Status is a pseudo entity related to the entity “Budget” in the system that is referred to as the status of the budget.

Definition of the behavior of Budget Status entity is defined in the Type Definition User Interface.

# Properties
Budget Status entity corresponds to “budget_status” table in the database which has the following fields:


| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|-|Auto generated
budget|Int|FK|Budget|The budget item's assigned budget|Auto assigned
account|Int|FK|Account|Assigned account of the budget item|Auto assigned
driver|Int|FK|Budget Driver|Assigned driver of the budget item|Dropdown
amount|Float|-|-|Budgeted amount for the budget item|User entry
details|JSON|-|-|-|Auto generated
version|Int|FK|Budget Version|Assigned version of the budget item|Auto assigned

# Default List
* Work in Progress
* Under Internal Review
* Under Audit
* Sent for Approval to RERA
* Final
