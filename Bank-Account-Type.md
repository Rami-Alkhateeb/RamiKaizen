# Definition

Bank Account Type is a pseudo entity related to the entity “Bank Account” in the system that is referred to as the type of the bank account.

Definition of the behavior of the entity is defined in the Type Definition User Interface.

# Properties

Bank Account Type entity corresponds to “bank_account_type” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List

* OA General Fund Bank Account
* OA Reserve Fund Bank Account
* Supplier Bank Account
* < < TODO > >
