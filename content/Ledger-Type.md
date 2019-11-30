# Definition
Ledger Type is a pseudo entity related to the entity “Ledger” in the system that is referred to as the type of the ledger.

Definition of the behavior of Ledger Type entity is defined in the Type Definition User Interface.

## Properties
Ledger Type entity corresponds to “ledger_type” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

## Default List
* General Ledger
* Tenant Ledger
* Landlord Ledger
* Unit SC Ledger
* Project Ledger
* OA Ledger
* Vendor Ledger