# Definition

Journal entries are the first step in the accounting cycle and are used to record all business transactions and events in the accounting system. As business events occur throughout the accounting period, journal entries are recorded in the “Ledger”.

# Properties

Journal Entry entity corresponds to “journal” table in the database which has the following fields:

| Property  | Type   | Reference | Reference To | Description | Method
| ------    | ------ | ------    | ------       | ------      | ------
id|Int|PK|-|Unique Identifier|Auto generated
journal_invoice|Int|FK|Invoice|-|Auto assigned
journal_account|Int|FK|Account|Assigned account|Auto assigned / Searchable Dropdown
journal_department|Int|FK|Department|Assigned department|Auto assigned / Searchable Dropdown
journal_cost_center|Int|FK|Cost Center|Assigned cost center|Auto assigned / Searchable Dropdown
journal_posted_by|Int|FK|Contact|Who posted the journal|Auto assigned
posting_date|Date|-|-|When the journal posted|Auto assigned
date|Date|-|-|Real transaction date|Datepicker
description|Text|-|-|-|User entry
debit|Float|-|-|Debit Value|Auto assigned / User entry
credit|Float|-|-|Credit Value|Auto assigned / User entry
journal_bank_account|Int|FK|Bank||Searchable Filtered Dropdown
bank_transaction_id|Text|-|-|-|Auto assigned / User entry

# Processes

## List

Journal entries are always listed as a line in the ledgers. The process is described in the “Ledger User Interface” section of this document.

## Create

There are two methods for creation, namely, Manual & Automated.

### Manual Create

Manual Journal Entry can only be used for non-standard cases. For

On the “Ledger User Interface” user has access to “Manual Entry” button. Upon click of this button a modal interface is shown as below:

![image](uploads/8035a3e0c4d89b9e99c4bd6747a77c55/image.png)

Ledger will be auto assigned as the screen is opened directly from the ledger screen.

Attachments will be listed using Listing Documents process, and can be added for a tenancy using Uploading Documents process.

Notes will be listed using Listing Notes process, and can be added for a tenancy using Creating Note process.

Cancel button cancels the process and returns to the previous screen while Save button initiates the transaction recording. 

* [ ] @alidikici Phase 2: According to the transaction’s account and ledger the behavior of posting to debit or credit changes. List all the possible scenarios and automate the entry’s side instead of entering debit / credit on the screen>

