MasterPlan uses Firestore database as the backend database of the whole system. 

Throughout this document the collections required for all the entities and processes will be listed with the field list and field required functionalities.

It should be noted that the Firestore pricing depends on the read/write and transfers from the database such as egress and ingress. Due to this nature of the Firestore database, developers should be careful about the number of writes and reads made to the database.

Throughout the documentation, the hints will be provided for the cost cutting approaches for the Firestore databases. However, developers should be careful about the implementation and should the feedback.