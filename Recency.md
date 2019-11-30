# Definition
Recency is a pseudo entity related to multiple entities in the system.

Definition of the behavior of Unit Type entity is defined in the Type Definition User Interface.

# Properties
Recency entity corresponds to “recency” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List
* New
* Current
* Old
