# Tenancy Status
Tenancy Status is a pseudo entity related to the entity “Tenancy” in the system that is referred to as the status of the tenancy.

Definition of the behavior of Unit Type entity is defined in the Type Definition User Interface.

## Recency Properties
Tenancy Status entity corresponds to “tenancy_status” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

## Recency Default List
* New
* Reserved
* Pending
* Upcoming
* Vacant
* Legal
