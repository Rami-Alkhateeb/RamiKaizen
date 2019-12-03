# Definition

Contact Function is a pseudo entity used wherever a Contact entity is assigned to any of the other entities. 

During the contact assignment, the user is expected to select a function for the assignment and the list provided below at the "Default List" should be presented to the user as a dropdown menu.

The list can be edited and/or reordered using the [Type Definition User Interface](Type-Definition-User-Interface).

# Properties

Contact Function entity corresponds to “contact_function” collection in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List

* Contractor
* Tenant
* Household
* Supplier
* Agent
* Owners Association Board Member
* Property Manager
* Building Manager
* Community Manager
* Portfolio Manager
* Broker
* Landlord
* Developer
* Board Member
* Budget Controller
* Budget Reviewer
* Auditor