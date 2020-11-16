---
id: 62b2aff3-626f-408d-a3dc-88a3a96d1084
title: Visualforce
desc: ''
updated: 1605526749981
created: 1603096143760
stub: false
---

# Visualsforce

## WHere
I can create VF pages in:
1. Setup
2. Developer console
3. VSCode extension

## Reference material
- [VF & Lightning Experience](https://trailhead.salesforce.com/content/learn/modules/lex_dev_visualforce)

## Viewing Visualforce Pages During Development:
accomplished by accessing the page using the https://yourInstance.salesforce.com/apex/PageName URL pattern.
Unfortunately, in Lightning Experience, I can only review the page but cannot test behaviour.

## How to test a VF page | [development](https://trailhead.salesforce.com/content/learn/modules/lex_dev_visualforce/lex_dev_visualforce_process):
1. create a tab for it
2. creating an "In development" app and add a tab to it.
App Manager-> New Lightning App (custom app)
From Setup -> App Menu -> select App Menu.You should see the App Menu Setup page.
Make sure that your In Development app is set to Visible in App Launcher.
Setup -> Tabs -> select Tabs.You should see the Custom Tabs Setup page.
Click New -> create a custom tab

<details><summary>
Reviewing Visualforce Pages in Multiple Environments
</summary>
 
**Main Development Environment**
This environment is where you work in Setup to make changes to your organization, like adding custom objects and fields, and maybe where you write actual code, if you use the Developer Console.
Browser: Chrome
User: Your developer user
User interface setting: Salesforce Classic

Review your page’s design and behavior in Salesforce Classic in this environment. **Lightning Experience Review Environment** This environment is where you check your page’s design and behavior in Lightning Experience.
Browser: Safari or Firefox
User: Your test user
User interface setting: Lightning Experience
**Salesforce Mobile Review Environment**
This environment is for checking your page’s design and behavior in the Salesforce app.
Device: iOS or Android phone or tablet
Browser: Salesforce app
User: Your test user
User interface setting: Lightning Experience
</details>

<details><summary>
For more ambitious projects, if you’re developing functionality that you need to support across a range of possibilities, take into consideration the need to test across:
</summary>
 Each different supported device.

 Each different supported operating system.
 Each different supported browser—including the Salesforce app, which embeds its own.
 Each different supported user interface context (Lightning Experience, Salesforce Classic, and the Salesforce app).
</details>

## Browser JS script to:
see the page I am working on:
```java {.line-numbers}
    $A.get("e.force:navigateToURL").setParams(
    {"url": "/apex/pageName"}).fire();
```
or from a prompt:
```java {.line-numbers}
    javascript:(function(){
    var pageName = prompt('Visualforce page name:');
    $A.get("e.force:navigateToURL").setParams(
        {"url": "/apex/" + pageName}).fire();})();
```

> Summary:
    - Development Mode for Visualforce is only available in Salesforce Classic
    - Test early, test often, test everything.

---

| classic | Lightning experience |
---------|----------|
| VF 'own' the page | VF run in an HTML 'iframe' |
==The point here is: Lightning Experience (/lightning) is in charge of the request.==
Session maintenance
- $Api.Session_ID
A “session” is basically some kind of token that your browser re-uses from request to request so that you don’t need to enter your username and password everytime. 
Scope inpact
Just remember:  Don’t touch other contexts’ stuff.
The **_#sforce.one_** JavaScript Utility Object, it provides a number of useful functions you can use in your own JavaScript code.
> Summary
Visualforce (visual.force.com) and Lightning Experience (force.com) are served from different domains
\<apex:page> showHeader and sidebar Attributes Are Always suppressed when pages run in Lightning Experience.

---

## [Managing VF navigation](https://trailhead.salesforce.com/content/learn/modules/lex_dev_visualforce/lex_dev_visualforce_navigation)
- button
- 'hidden' code in SF based on events happening (ex. triggered navigation due to select a value in a picklist)
- custom code that control the application flow
#### Navigation Gotchas
1. do not set #window.location directly.
That works only in SF Classic, in Lightning, VF pages are an iframe tag, so you cannot use it. It does not work.
2. Don’t use static URLs to Salesforce resources:
    * In Visualforce markup, use {!URLFOR($Action.Contact.Edit, recordId)}
    * In JavaScript, use navigateToSObject(recordId)


Summary
> PageReference take trace of the navigation in Classic; that currently works in Lightning but not best practice... where #JavaScript is.
window.location don't work in Lightning experience
navigateToSObject(recordId) is not available for Classic

---

## Features to Avoid in Lightning Experience
In VF:
- Lightning Experience Header and Navigation Menu Can’t Be Suppressed
- Salesforce Classic Header and Sidebar Are Always Suppressed
But remember:
> the showHeader and sidebar attributes of <apex:page> have no effect on 
Visualforce pages when displayed in Lightning Experience

Components to avoid using in Lightining for VF pages:
 - some related lists in Lightining are blocklisted (not supported) using the tag:#<apex:relatedList> 
 - #<apex:iframe> is supported but better to avoid using it since 

Summary
> Don’t Set window.location Directly

---

## Design for VF & LX

- [trailhead](https://trailhead.salesforce.com/content/learn/modules/lightning_design_system)
