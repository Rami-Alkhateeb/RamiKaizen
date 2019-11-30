# Definition

Budget Status is a pseudo entity related to the entity “Budget” in the system that is referred to as the status of the budget.

Definition of the behavior of Budget Status entity is defined in the Type Definition User Interface.

# Properties
Budget Status entity corresponds to “budget_status” table in the database which has the following fields:


| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List
* Work in Progress
* Under Internal Review
* Under Audit
* Sent for Approval to RERA
* Final
