# Cost Center

## Cost Center Properties

Cost Center entity corresponds to “cost_center” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|Unique Identifier|Auto generated
name|Text|-|-|Name of the cost center|User entry
cost_center_project|Int|FK|project|Project of the cost center|Searchable Dropdown
hasGeneralFund|Bool|-|-|-|Checkbox
hasReserveFund|Bool|-|-|-|Checkbox
description|Text|-|-|-|User entry
cost_center_entitlement_type|Text|FK|Entitlement Type|Entitlement Type|Dropdown
entitlement_type_reason|Text|-|-|-|User entry
aggregate_entitlement|Calc|-|-|-|-
notice_text|Text|-|-|-|User entry
isPenaltyApplicable|Bool|-|-|-|Checkbox
isVATFreeSCAllocation|Bool|-|-|-|Checkbox
date|Date|-|-|-|Date Picker
mollak_id|Text|-|-|-|User entry
mollak_name|Text|-|-|-|User entry
mollak_sc_usage|Text|-|-|-|User entry

## Cost Center Processes

### Cost Center Listing

System should list the cost centers under the currently active project in a tabular format as represented below:

![image](uploads/3debe1a41d59f00829dbc69693a63dd0/image.png)

Click action on any of the columns should open a modal UI and display the cost center details as described at the Editing a Cost Center / Cost Center Details section of this document.

Click action on “Create” button initiates Creating a Cost Center process.

### Cost Center Create

![image](uploads/caf2f831d415d57bdae73a1392c7e24d/image.png)

When “Create” button is clicked on the “Listing Cost Centers” screen, a modal dialog opens and asks only for the “Name” of the new cost center. 

Two buttons on the modal screen should exist. 
* Create: Creates the cost center. Following the creation, system takes the user interface to the newly created cost center details screen as explained below.
* Cancel: Cancels the creation and rolls back to cost center listing.

### Cost Center Edit/View

![image](uploads/8edc3af6836a61b3ff5ba2eac038e114/image.png)

![image](uploads/592422847079af6b5835cdcf61884234/image.png)

Name: Name of the cost center.

Project: The project of the cost center.

Has General Fund: Checkbox.

Has Reserve Fund: Checkbox.

Entitlement Type: Dropdown list of the “Entitlement Type” entity.

Entitlement Reason: Text user entry.

Aggregate Entitlement: Dynamically calculated as a sum of square footage of all the descendant units.

Penalty Applicable: Checkbox.

VAT Free SC Allocation: Checkbox.

Date: Date Picker.

Mollak ID: The identifier used to integrate with the Mollak system.

Mollak Name: Textual name of the cost center in the Mollak system.

Mollak SC Usage: Textual user entry.

Notice Text: Edited using a rich text box editor via a modal screen interface.

Description: Edited using a rich text box editor via a modal screen interface.

Attachments will be listed using Listing Documents process, and can be added for a Cost Center  using Uploading Documents process.

Notes will be listed using Listing Notes process, and can be added for a Cost Center  using Creating Note process.

Assign Units: Click action of the “Assign Units” button on the cost center detail screen should open a new modal UI and represent the list of unassigned units. From this list user should be able to assign the available units to the cost center.
