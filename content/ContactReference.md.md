# Contact Reference

Contact Reference entity defines the relationships between a Contact and other entities. Since a contact can be referred by multiple other entities, and an entity can have multiple contacts with varying types, the Contact Reference pseudo entity is defined in the system to handle these many to many relationships.


# Properties

Contact Reference entity corresponds to “contact_reference” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|Unique Identifier|Auto generated
contact_reference_contact|Int|FK|Contact|Dropdown|User entry
contact_reference_function|Int|FK|Contact Function|Dropdown|Read-only
contact_reference_reference|Int|FK|Reference|Dropdown|Read-only
referrer|Int|FK|Many|Check below description|Read-only


# References

Each contact that is created in the system has to have a referrer and a Reference. 

Reference denotes to the entity that the contact is bound to. Such as, if the Reference is Unit, the contact is a Unit’s contact, and if the Reference is Building, the contact is a Building’s contact.

Referrer is the id of the referring Entity. Such as, if the Reference is Unit and the referrer is 192, this means that the contact is bound to the Unit which has the id field value as 192.

This handles the many-to-many relationships between contacts and other entities defined in the system. The process denoted is “Assign Contact” for this functionality. 



