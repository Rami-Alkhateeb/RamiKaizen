# Definition

A persona is a system user in which interacts with the system. Each individual persona has certain ways of using the system. 

A persona shouldn’t be confused with the “User” entity defined in this document. While a user represents merely a login credential, a persona is the definition of the roles and actions in the system. In the following parts of this design document, the list of personas will be represented with their corresponding interactions.

When the user logs into the mobile application with his email id and password system will identify the contact entries referencing the user with a FK and assign the correct personas to the user for the session. 

## Tenant Persona
Tenant persona represents the contacts in the system which are assigned.

If the user is tenant of multiple units, system should provide a selection screen in order for the tenant to be able to use the system for all the units.

This persona is responsible for providing the below documents to the system for himself/herself and also the household of the unit. System should provide functionality to upload these documents:
* National ID Copy
* Passport Copy

This persona is required to provide car plate number for himself/herself and also for the household of the unit.

This persona can view the tenancy agreement and attached documents and other uploaded documents.

This persona is required to provide a digital signature to the system to be used by the system. Since system auto generates the tenancy contract, the signature should be placed at the required part of this document.

If the project/building of the tenancy agreement’s unit has an access management system managed by the system, phone application of the user should provide below functionalities:

* Parking gate access via phone application or plate reader:
  * System should provide the necessary information to the user about the assigned entrance and exit gates.
* Facility access via phone application:
  * System should provide the information about the facilities in the unit’s building and project in order for tenant to have an efficient access to these facilities.
* Facility booking via system (Phase 2):
  * Tennis Court Booking
  * Sauna/Steam Room Booking
    * If the person is using the sauna, and hasn’t vacated the sauna after 15 minutes, the security personas should be notified about the situation to protect the health of the person.

**View Account Statement:** Tenant should be able to see the account statement.

**Request Document Collection:** Some of the documents can’t be accepted in a digital format. In this case, user should be able to request a document collection from the team. However in some buildings we will be having document collection boxes. In this case, application should be directing the user to use an envelope and drop the documents to the collection box.

**Payment Services**
* Tenant should be able to make the tenancy payments from the system.
* Tenant should be able to make the value added services payments from the system.

**Value Added Services**
* Car Wash Service Arrangement
  * If the building of the unit has an assigned car wash vendor, user should be able to arrange the car to be washed.
* Finding a personal trainer
* Find a house cleaning service
* Meeting room booking
* Function room booking
* Co-working space booking
* Laundry service booking
* Tutoring booking
* Child care booking
* Pet care booking
* Household needs delivery service (grocery, IT services etc.)
* Relocation booking
* Catering delivery (such as Kitopi)
* Phase 2: Flea Market (maybe users should be able to search through the whole system).
* Other value added services will be defined as they are taken into consideration for the system (Phase 2).

**Initiate Work Order and Snag Pictures:** In case there is an issue with the unit, or there is a requirement for maintenance this persona should be able to take the pictures of the issue and write a description of the request. User should also choose the nature of the work and the work order gets created.

- [ ] Provide the diagram

**Initiate Request:** List of possible requests can be found below
* Move-in request
* Move-out request
* Delivery request

**Call for Security:** In the case of emergency and assistance requirement, tenant should be able to call for security attendance.

**Contact Call Center:** In the need of any requirement that is not listed above, system should provide a communication channel directly connected to our call center agents.

**Bring People Together (Phase 2):** User can announce and search for partners in below activities:
* Gym buddy finding
* Squash/Tennis buddy finding
* Yoga Group
* Children playtime friend finding

**Rent out Tenancy Resources (Phase 2):** A tenant should be able to rent his extra parking space and/or storage space to the other residents.

## Household Persona

In some situations in the same unit there are multiple individuals living. Such as wife, husband, partner, children. 
If the persona is 18 or more years of age, he/she will be able to perform the below tasks as defined in the “Tenant Persona” section of this document:
* * Document upload and view
* Provide digital signature
* Utilize Access management
* Utilize facilities
* Utilize value added services
* Initiate work order
* Initiate request
* Payment services
* View account statement
* Call for security
* Contact call center
* Request document collection
* Bring people together

## Landlord Persona
Landlord should be able to access the below functionalities:
* Provide digital signature
* Document upload and view
    * Emirates ID
    * Title Deed
    * Management Contract
* Digitally sign management contract
* Initiate and approve work order
* Payment services
* View account statement
* View units/tenants/household/unit & tenancy documents
* Landlord should be provided with a cash flow chart, including past and foreseeable future which has a click action to take the user to the payment schedule details screen which includes all the monetary transactions including but not limited to rent, maintenance, management fees, etc..
* Request document collection.

## Traveller Persona
To be utilized for travel homes concept.
- [ ] Provide definition

## Vendor Company Persona
- [ ] Provide definition

## Vendor Supevisor Persona
- [ ] Provide definition

## Portfolio Manager Persona
- [ ] Update Definition @ariza

If the user's contact function is Portfolio Manager, below feautures wil be enabled:

* User should be able to view the list of Units, Unit Details and Tenants of each unit
* If the unit is occupied, he should be able to view the Tenancy Contract of the units
* Portfolio Manager should be able to view each unit's payment schedule, Total Rent, Rent paid, Rents Upcoming/Pending
* Portfolio Manager should be able to view the Maintenance costs for his units
* Portfolio Manager should have dashboard of his units' status, showing Leased and Vacant Units

## Community Manager Persona

If the user's contact function is Community Manager, below features will be enabled:

* User should be able to view the list of Reqests created by Tenants or Owners for the Community he is managing
* Different sections to view differet requests: Movein/Moeout, Workpermit, Service Charge Clearance, Access and Barrier remote
* User should be able to approve or reject the requests
* User should get new notifications whenever new requests has been created for the community

