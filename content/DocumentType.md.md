# Document Type

Document Type is a pseudo entity related to the entity “Document” in the system that is referred to as the type of the document.

Definition of the behavior of Document Type entity is defined in the Type Definition User Interface.

# Properties

Document Type entity corresponds to “document_type” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
name|Text|PK|-|Name of the Type|Auto generated
position|Int|-|-|Position of the type in the list in any UI Component|Drag&Drop

# Default List

* Title Deed
* Marketing Image
* National ID
* Visa
* Passport
* Tenancy Contract
* Invoice

# Related Notifications

Some of the document types require system to send notifications to the related parties. The requirements are listed below:

## National ID Document Requirements

National ID is the government issued document to the residents of the country. In the UAE name of the document is the Emirates ID, however system is required to be international and should be all encompassing.

National ID has an issue date and in some countries, an expiry date. System user should be able to define these dates for this type of document. 

Notification Date property of the tuple will be automatically set to 30 calendar days before the expiry date.

< < < TODO > Design the notification message template > >

## Visa Document Requirements

Work/Residence visa is the government issued document to the expatriates of the country. 

The visa document has an issue date and an expiry date. System user should be able to define these dates for this type of document.

Notification Date property of the tuple will be automatically set to 30 calendar days before the expiry date.

 < < < TODO > Design the notification message template > >

## Passport Document Requirements

Passport is the government issued document for all individuals by their home country. 

The passport document has an issue date and an expiry date. System user should be able to define these dates for this type of document.

Notification Date property of the tuple will be automatically set to 30 calendar days before the expiry date.

< < < TODO > Design the notification message template > >

## Tenancy Contract Document Requirements

Tenancy contract document doesn’t require any dates assigned to it since it is directly attached to the Tenancy entity, and this entity has its own set of dates and notification settings.

## Invoice Document Requirements

Invoice document doesn’t require any dates assigned to it since it is directly attached to the Invoice entity, and this entity has its own set of dates and notification settings.

