---
id: a2b154f3-79f5-49bc-8e95-451df731715e
title: Trigger
desc: ''
updated: 1605097693508
created: 1602596666973
stub: false
---

# ask yourself
- When to use triggers?
- what they are?

((ref: [[computer-science.lang.apex.templates]]#Trigger:#end-trigger))

> A trigger is code in Apex that '_**trigger**_' the execution of a piece of code.

## trigger requirements:
- trigger class
- test class

> explained like to a 5 yo: a trigger is like a car, in order to run on the street and don't kill anyone, you have to be sure that the car is safe to drive for you and for the sake of other people.

#### Demo: Write a basic Apex trigger
    - Line by line explanation
    - See our trigger in action
```java
// we create a trigger called helloWorld that fire before the trigger is updated
trigger helloWorld on Lead (before update) {
    // trigger loop to update trigger in bulk
    // Trigger.new is the list of all leads in this trigger
    // for each trigger assigned to a variable 'l' assign:
    for (Lead l : Trigger.new){
        // logic of the trigger in the scope
        l.FirstName = 'Hello';
        l.LastName = 'World';
    }
}
``` 
#### The trigger loop, explained
I need a loop since users can do different 'bulk' operations on the data using Data Loader, Dataloader.io, Workbench
Remember the #Governor-limits and limits for SOQL (200), DML (150) etc.

#### Demo: Write a trigger!
> Write a trigger that creates a task for each new opportunity: 
- Subject: "Apple Watch Promo"
Description: "Send one ASAP!"
Priority: "High"
- Related To: our opportunity

the code:
```java
    trigger AppleWatch on Opportunity (after insert) {
    for(Opportunity opp: Trigger.new){
        Task t = new Task();
        t.Subject = 'Apple Watch Promo';
        t.Description = 'Send one ASAP!';
        t.Priority = 'High';
        t.WhatId =  opp.Id;
        insert t;
    }
}
```

When to use before vs. after triggers

**Before**
#### is more safe!
PROS: No need to explicitly save your work, the save event is coming
CONS: System level fields are not available, they're not populated 
**After**
PROS: System fields now available:
Record ID (insert), Created Date (insert), Last Modified Date (update)
CONS: Need to explicitly save your changes, Potentially create infinity loops

```
start -----------------+------------------ finish
       before trigger  |   after trigger
                    record saved
```

#### infinite trigger!!!
```java
    trigger infinite on Opportunity (after update) {
    for(Opportunity opp: Trigger.new){
        opp.amount =  1.000;
        update opp;
        // after the DMl statement the cycle start again
        // SF orevent this error with a read-only record
    }
}
```

#### How this trigger should be written?
```java
    trigger infinite on Opportunity (before update) {
    for(Opportunity opp: Trigger.new){
        opp.amount =  1.000;
    }
}
```
#### trigger Id not available:

```java
trigger NonExistentId on Case (before insert) { 
    for (Case myCase : Trigger. new) { 
        CaseComment cc = new CaseComment() ;
        cc.CommentBody = 'Case received by Agent';
        // basically we try to set the ParentId for the Case but the Id is assign to a value that doesn't exist yet since we still have to insert the cc
        // myCase.Id is still EMPTY!
        cc.ParentId - myCase.Id;
        insert cc;
    }
}
```
- to fix it we just need to use an after insert trigger!


<details><summary>
Demo: Write a trigger!
</summary>

exercise:
Write a trigger that does the following when an Account is created: Create a new case
Assign the owner to your new intern
Subject: Dedupe this account
Associate with the account

```java
trigger testNewCase on Account(after insert) { 
        for (Account acct: Trigger.new) {
             // Create an object (optional)
             Case c = new Case();
             // Update record
             c.Subject = 'Dedupe this account';
            // Set the owner of the case to a specific person/user
             c.OwnerId = '0034K0000021eQ5QAI';
             c.Status = 'New';
             // associate a Case to Account
             c.AccountId = acct.Id;
             // Explicit save (optional)
            insert c;
        }
```
</details>

