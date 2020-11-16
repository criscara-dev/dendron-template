---
id: 8fc05bfe-2f9f-470e-839f-8eb7ffd6f61b
title: Development
desc: ''
updated: 1605377502064
created: 1604931859400
---

## The main resource for a developer in SF

<details><summary>
What is a sandbox?
</summary>

![](/assets/images/2020-11-09-14-25-38.png)
</details>

<details><summary>
How you develop in SF?
</summary>

Using the MVC pattern
==MODEL== -> the databse (schema)
==VIEW== -> the UI
==CONTROLLER== -> the business logic (using declarative or programmatic tools)

![](/assets/images/2020-11-09-15-44-39.png)
</details>
<br>
Know the difference between [[standard-object]] and [[custom-object]]

What is the difference between data and [[metadata]]?

```mermaid
    flowchart LR
    Accounts -- relationship --x Contacts
```

<details><summary>
What are relationships and how to use them?
</summary>

The relationship is defined on the child object using a custom field.
These are the types of relationship fields:
- Master-Detail
- Lookup

![](/assets/images/2020-11-09-15-29-00.png)
</details>


<details><summary>
What do you need in a many-to-many relationship?
</summary>

You need a Junction Object
```mermaid
    flowchart LR
    A[Certifications] x--x B
    B[Junction Object] x--x C[Contacts]
```
</details>

<details><summary>
Keys takeways on Objects
</summary>

- Objects represent database tables that contain your organization's information.
- Objects created by Salesforce are called standard objects. 
- A custom object is an object you create to capture and manage additional data based on your specific business requirements. 
- Object access determines which objects users can view and edit. 
- Record access determines which individual records users can view and edit in each object on which they have been granted appropriate permissions. 
- Standard and custom fields store data on individual records. 
- Create lookup or master-detail relationships to model one-to-many relationships in Salesforce. 
- Use junction objects to model many- to-many relationships.
</details>

<details><summary>
What can an Object allow you to do?
</summary>

Objects on the Lightning Platform:
- Provide a predefined set of standard
fields to capture common business
information.
- Allow you to create custom fields
to capture additional business
information.
- Allow you to create custom
relationships to link objects together.
- Allow you to create validation rules
to verify that the data in one or more
fields meets the specified criteria
before the record is saved.
- Allow you to define page layouts and
record types to control what a user
sees when they view or edit a record.
- Allow you to automate business
processes using workflow rules,
processes, flows, and approval
processes.
- Allow you to control record access
and field-level security.
</details>

