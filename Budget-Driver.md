# Definition

Budget Driver is a pseudo entity related to the entity “Budget Item” in the system that is referred to as the driver of the budget item.

Definition of the behavior of Budget Driver entity is defined in the Type Definition User Interface.

# Properties
Budget Driver entity corresponds to “budget_driver” table in the database which has the following fields:


| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List
* Equal Division
* Entitlement
* Manual
