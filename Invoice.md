# Definition
Invoices are used for AP and AR ledgers at the current phase of the project

Property         | Type    | Reference To | Description               | Method
------           | ------  | ------       | ------                    | ------
id               | string  | -            | -                         | Auto assigned by firestore
invoice_number   | string  | -            | -                         | User entry
type             | string  | invoice_type | sub-collection of types   | Dropdown
invoice_date     | number  | -            | yyyymmdd                  | User entry
due_date         | number  | -            | yyyymmdd                  | User entry
contact          | string  | contacts     | -                         | Dropdown
description      | string  | -            | -                         | User entry
amount           | number  | -            | -                         | User entry
amount_paid      | number  | -            | -                         | User entry
balance          | number  | -            | -                         | Auto calculated
printed          | boolean | -            | -                         | Checkbox
accrued          | boolean | -            | -                         | Checkbox
accrued_from     | number  | -            | yyyymmdd                  | User entry
accrued_to       | number  | -            | yyyymmdd                  | User entry
unit             | string  | units        | get project units element | Dropdown