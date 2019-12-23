# Definition

Contact Reference entity defines the relationships between a Contact and other entities. Since a contact can be referred by multiple other entities, and an entity can have multiple contacts with varying types, the Contact Reference pseudo entity is defined in the system to handle these many to many relationships.

# Properties

Contact Reference entity corresponds to “contact_reference” collection in the database which has the following fields:

```
"id<uuid()>": {
    "contact": <Contact uuid as stored in the contacts collection>,
    "reference": <Please refer to below description>,
    "function": <Reference id as stored in the types collection contact_functions object>
}
```

# References
Each contact reference object stored in the database binds a contact to an entity with a function.  
"reference" field in the object corresponds to the address of the reference, such as:

* Tenant Reference:
```
"uuid": {
    "contact": "<contact_uuid>",
    "reference": "<project_uuid/units/unit_uuid/tenancies/tenancy_uuid>,
    "function": "tenant"
}
```

* Household Reference (if unit is rented/leased):
```
"uuid": {
    "contact": "<contact_uuid>",
    "reference": "<project_uuid/units/unit_uuid/tenancies/tenancy_uuid>,
    "function": "household"
}
```

* Household Reference (if unit is used by landlord):
```
"uuid": {
    "contact": "<contact_uuid>",
    "reference": "<project_uuid/units/unit_uuid/landlords/landlord_uuid>,
    "function": "household"
}
```

* Landlord Reference:
```
"uuid": {
    "contact": "<contact_uuid>",
    "reference": "<project_uuid/units/unit_uuid/landlords/landlord_uuid>,
    "function": "landlord"
}
```