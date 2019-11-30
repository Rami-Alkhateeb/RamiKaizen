# Definition

Contact Type is a pseudo entity related to the entity “Contact” in the system that is referred to as the type of the document.

Definition of the behavior of the entity is defined in the Type Definition User Interface.

# Properties

Contact Type entity corresponds to “contact_type” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List

* Individual
* Internal Company
* Vendor Company
* Client Company

