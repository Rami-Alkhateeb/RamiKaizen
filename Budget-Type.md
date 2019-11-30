# Definition

Budget Type is a pseudo entity related to the entity “Budget” in the system that is referred to as the type of the budget.

Definition of the behavior of Budget Type entity is defined in the Type Definition User Interface.

# Properties
Budget Type entity corresponds to “budget_type” table in the database which has the following fields:


| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List
* Normal Budget
* Special Budget