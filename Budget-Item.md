# Definition

Each budget item is the line-item in the budget study that is entered by the system users.

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

# Default List
* Work in Progress
* Under Internal Review
* Under Audit
* Sent for Approval to RERA
* Final
