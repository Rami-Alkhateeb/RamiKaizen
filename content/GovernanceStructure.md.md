# Governance Structure

Governance Structure is a pseudo entity related to the entity “Project” in the system that is referred to as the governance structure of the project’s owners association .

Definition of the behavior of Governance Structure entity is defined in the Type Definition User Interface.

# Properties

Governance Structure entity corresponds to “governance_structure” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List

* Stand Alone Scheme
* Top Level Scheme
* Second Level Scheme
* Third Level Scheme
* Unlimited
* Limited
* Limited that has limited
