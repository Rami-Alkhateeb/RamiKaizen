# Tenancy

## Tenancy Properties
Tenancy entity corresponds to “tenancy” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|Unique Identifier|Auto generated
unit|Int|FK|Unit|Leased Unit|Searchable Dropdown
landlord|Int|FK|Landlord|Landlord of the unit|Searchable Dropdown
type|Int|FK|isCurrent|Type of the tenancy|Dropdown
deposit|Float|-|-|Received Deposit from the tenant|User Entry
annual_rent|Float|-|-|-|User Entry
contract_value|-|-|-|-|Auto Calculated
installments|Int|-|-|Number of cheques per year|User Entry
agency_fee|Float|-|-|-|User Entry
renewal_fee|Float|-|-|-|User Entry
ejari_fee|Float|-|-|-|User Entry
start|Date|-|-|Start Date of the tenancy|Date Picker
end|Date|-|-|End Date of the tenancy|Date Picker
contract_number|Text|-|-|-|User Entry

## Tenancy Processes

### Tenancy Listing

![image](uploads/333cf9920e583df837d3be7410a63ad5/image.png)

* [ ] Phase 2: Tenancy can span multipl years, and year over year there is a rent increase. This should be handled by the system. @ariza

Leasing tab uses an accordion UI interface to display the future, current and past leases. 

Tenancies are descending ordered by end date.
By default, when the tab is visited, currently active lease details are expanded in the accordion UI and user can click to collapse and expand the individual accordion panels.

Attachments will be listed using Listing Documents process, and can be added for a tenancy using Uploading Documents process.

Notes will be listed using Listing Notes process, and can be added for a tenancy using Creating Note process.

Generate Lease Agreement button should be enabled for the Lease if the tenancy contract is not already uploaded to the system.  Lease agreement document will be generated as per the Ejari Template.

System should provide facility to assign multiple Contacts as the tenants and also system should provide the facility to assign household individuals to the tenancy definition. Examples would be the partner, maid or family of the tenant. 

### Tenancy Create

![image](uploads/fe48c736566da7a94b89d4fd22553dd6/image.png)

On the Leases tab of the unit details UI, “New Lease” button opens a modal screen asking for start and end dates of the new tenancy. Both dates should provide the date picker UI component for data entry. If the cancel button is clicked, the process is cancelled. If the OK button is clicked, the system creates a new record in the tenancy table of the system database with the provided dates of the tenancy and mark the tenancy as a new tenancy. Once the database insert operation is complete, the system takes the user automatically to the new tenancy details to be edited.

### Tenancy Archive

On the Leases tab of the unit details UI, “Archive” button on the current lease screen asks for confirmation from the user and updates the deleted_at field of the tuple with the current timestamp.

### Assign Current
On the Leases tab of the unit details UI, if the current state of the system UI shows a “new lease”, an additional button “Assign Current” is displayed to the user. Click of this button requests confirmation from the user and changes the type field of the tuple to current lease in the system database as well as changes all the other tenancy tuples assigned to the current unit as archived.
