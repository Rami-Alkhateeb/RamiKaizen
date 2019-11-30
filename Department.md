# Definition

Each journal in the all of the ledgers utilize a department as the identifier to describe the assignment of the transaction. 

Definition of the behavior of Department entity is defined in the Type Definition User Interface.

# Properties

Account entity corresponds to “account” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
code|Text|PK|-|User entry|Auto assigned
name|Text|-|-|User entry|Auto assigned / Searchable Dropdown
parent|Text|FK|Account|Searchable Dropdown|Auto assigned / Searchable Dropdown
position|Int|-|-|Position of the type in the list in any UI component|Auto assigned

System should only enable the data entry for the level 0 (non-parent) departments throughout the system. Parent departments are only utilized as a summary and aggregation level.

# Default List

List of the departments required as the default system will be provided in a separate document.
