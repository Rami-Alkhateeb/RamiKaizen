# Building

## Building Properties
Building entity corresponds to “building” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|Unique Identifier|Auto generated
name|Text|-|-|Name of the building|User entry
project|Int|FK|project|Project of the building|Searchable Dropdown
floors|Int|-|-|Number of Floors in the building|User entry
aggregate_entitlement|Float|-|-|Total square footage|Dynamic Calculation
present_use|Text|-|-|-|Dynamic Calculation
aggregate_entitlement|Float|-|-|Total entitlements as an aggregate|Dynamic Calculation
certification_of_occupation_on|Date|-|-|-|Date Picker
address|JSON|-|-|-|Google Maps
warning_message|Text|-|-|-|User entry
access_management_definitions|JSON|-|-|Phase 2|Phase 2

## Building Processes

### Building Listing

System should list the buildings under the currently active project in a tabular format as represented below:

![image](uploads/5352aa9c6b0a994ae8739a1f268e2733/image.png)

Click action on any of the columns should open a modal UI and display the building details as described at the Editing a Building / Building Details section of this document.

Click action on “Create” button initiates Creating a Building process.

### Building Create

![image](uploads/827d7a58c8e7c49dcf3912de8b718e32/image.png)

When “Create” button is clicked on the “Listing Buildings” screen, a modal dialog opens and asks only for the “Name” of the new building. 

Two buttons on the modal screen should exist. 
* Create: Creates the building. Following the creation, system takes the user interface to the newly created building details screen as explained below.
* Cancel: Cancels the creation and rolls back to building listing.

### Building View/Edit

![image](uploads/a6db1327a3663302cd01ec2569612045/image.png)

Name: Name of the building.

Project: The project of the building.

Floors: Numeric user data entry.

Number of Units: Dynamically calculated as a result of unit assignment as described in the Units Tab of the project details.

Aggregate Entitlement: Dynamically calculated as a sum of square footage of all the descendant units.

Present Use: This is the dynamically curated information of the units as an aggregation. Lists all the distinct unit types under the given building.

Certification of Occupation Date: Date picker

Address: Address of the building. Edit button next to address opens the Address selection/creation UI on a modal screen.

Warning Message: Edited using a rich text box editor via a modal screen interface.

Developer: Developer is assigned to the Building  using “Assigning Contact” process.

General Manager: General manager is assigned to the Building  using “Assigning Contact” process.

Portfolio Manager: <<TODO> Does a project has a portfolio manager> Portfolio manager is assigned to the Building  using “Assigning Contact” process.

Community Manager: Community manager is assigned to the Building  using “Assigning Contact” process.

Building Manager: Building manager is assigned to the Building  using “Assigning Contact” process.

Attachments will be listed using Listing Documents process, and can be added for a Building  using Uploading Documents process.

Notes will be listed using Listing Notes process, and can be added for a Building  using Creating Note process.

* [ ] Access management Phase 2: If the unit is travel house, access should be managed @ariza
