---
id: bdf0d0a4-e383-4d9b-8d12-7c79a9645919
title: JavaScript Developer 1
desc: ''
updated: 1611086632232
created: 1610206576325
---

## JavaScript Developer 1 Certification

### References:
[JS Trailmix](https://trailhead.salesforce.com/users/strailhead/trailmixes/prepare-for-your-salesforce-javascript-developer-i-credential)

[Module:JavaScript Skills for Salesforce Developers](https://trailhead.salesforce.com/content/learn/modules/javascript-essentials-salesforce-developers?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)

[Module:Modern JavaScript Development](https://trailhead.salesforce.com/content/learn/modules/modern-javascript-development?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)


[Lightning Web Components Basics](https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics)


- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force.htm)
---
[CLI](https://trailhead.salesforce.com/content/learn/modules/cli-basics?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
Notes:
Command ex.:

```terminal
 $ command -flag arguments
```
![](/assets/images/2021-01-18-08-55-39.png)
* The command is: sfdx force:project:create
* The flag -n is required and tells the system what to name your new project.
* The argument is MyProject which is the name we are assigning to the project.
* Switches are a lot like flags but don't require arguments. Switches are identified by two hyphens -- and followed by a value.

- Install last version _npm_: 

```terminal
npm install npm@latest -g
```
- Update sfdx:
```terminal
sfdx update
```

- [SFDX](https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
Notes:

<details><summary>
What Is a Scratch Org?
</summary>
in SFDX, A scratch org is a dedicated, configurable, and short-term Salesforce environment that you can quickly spin up when starting a new project, a new feature branch, or a feature test.
</details>

<details><summary>
What Is a Developer Hub Org?
</summary>
A Developer Hub (Dev Hub) is the main Salesforce org that you and your team use to create and manage your scratch orgs
</details>

Basic Commands in SFDX:
```
SFDX
Usage: sfdx COMMAND [command-specific-options]
 Help topics, type "sfdx help TOPIC" for more details:
 sfdx force # tools for the salesforce developer
 sfdx plugins # manage plugins
 sfdx update # update sfdx-cli
```
- create a Dev Hub:
```
sfdx auth:web:login -d -a DevHub
```
... and then Allow.

- to get help:
```
sfdx force --help
```
- create a scratch org:
```
Create a scratch org, set it as your default, and give it an alias
```
- delete an org:
```
sfdx force:org:delete
```
Display a list of all authorized orgs. You should see an entry listed with alias DevHub
```
sfdx force:org:list
```
[Use this Dev Hub as the default](https://trailhead.salesforce.com/content/learn/projects/develop-app-with-salesforce-cli-and-source-control/set-up-your-environment?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential#authorize-dev-hub-org-with-the-salesforce-cli:~:text=Use%20this%20Dev%20Hub%20as%20the%20default) for all Salesforce DX projects on this computer so that you don’t have to specify the --targetdevhubusername | -v CLI argument for each command
```
sfdx config:set defaultdevhubusername=DevHub --global
```
![](/assets/images/2021-01-18-11-22-49.png)

<details><summary>
Ex. SQOL to retrieve sample data from Devhub Org
</summary>

```apex
sfdx force:data:tree:export --targetusername DevHub --outputdir assets/data --query "SELECT Id, Name, Email__c, Phone__c, Mobile_Phone__c, Title__c, Picture__c, ( SELECT Id, Address__c, Assessed_Value__c, Baths__c, Beds__c, Broker__c, City__c, Date_Agreement__c, Date_Closed__c, Date_Contracted__c, Date_Listed__c, Date_Pre_Market__c, Description__c, Location__Longitude__s, Location__Latitude__s, Picture__c, Price__c, Name, State__c, Status__c, Tags__c, Thumbnail__c, Title__c, Zip__c FROM Properties__r ) FROM Broker__c"
```
</details>

[how to disable caching in any (scratch, dev, sandboxes...) Org](https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/debug_disable_caching.htm)
![](/assets/images/2021-01-18-12-13-02.png)

[Import & Export data between Orgs](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_test_data_example.htm)

[Create a new SFDX project](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_ws_create_new.htm)

Delete a Scratch org command:
```
sfdx force:org:delete
```
create a Scratch Org:
```
sfdx force:org:create --setdefaultusername --setalias sfdx-chan --definitionfile config/project-scratch-def.json
```
Push local source metadata to scratch org.
```
sfdx force:source:push
```

---
[Coding for Web Accessibility](https://trailhead.salesforce.com/content/learn/modules/coding-for-web-accessibility?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
Notes:
Semantic MarkUp:
[Nu HTML Checker](https://validator.w3.org/nu/)
Remember: roles,states,properties
[Global focus guidelines](https://www.lightningdesignsystem.com/accessibility/guidelines/global-focus/)
[Accessibility Object Model](https://wicg.github.io/aom/spec/)
[Web Components](https://www.webcomponents.org/introduction)

---
[Lightning Design System for Developers](https://trailhead.salesforce.com/content/learn/modules/lightning_design_system?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
Notes:
[lightningdesignsystem.com](https://www.lightningdesignsystem.com/)
BEM system:
* A block represents a high-level component (e.g. .car)
* An element represents a descendant of a component (e.g. .car__door)
* A modifier represents a particular state or variant of a block or element (e.g. .car__door_red)
Grid System
[CSS-tricks flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
Data:
-  in the current release the Design System doesn’t support built-in Visualforce components — the <apex:*>, <chatter:*> and other components
- the use of [Remote Objects,](https://developer.salesforce.com/docs/atlas.en-us.pages.meta/pages/pages_remote_objects.htm) JavaScript Remoting or the REST API to access Salesforce data from your Visualforce pages based on Design System markup
Avatar, Icons and [SVG Sprite](https://css-tricks.com/svg-sprites-use-better-icon-fonts/)

<details><summary>
What is a Card and a Tile component?
</summary>

A [tile](https://www.lightningdesignsystem.com/components/tiles/) is a grouping of related information associated with a record.
[Cards](https://www.lightningdesignsystem.com/components/cards/) are used to apply a container around a related grouping of information.
</details>

---

[Quick Start: Lightning Web Components](https://trailhead.salesforce.com/content/learn/projects/quick-start-lightning-web-components?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential): easy and quick way to start with a basic LWC HelloWorld component

---

[Lightning Web Components Basics](https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
Notes:
https://webcomponents.dev/
- To develop Lightning web components efficiently, use the following tools and environments.
1. Dev Hub and Scratch Orgs
2. Salesforce Command Line Interface (CLI)
3. [Lightning Component Library](https://developer.salesforce.com/docs/component-library/overview/components)
4. [Lightning Web Components Recipes ](https://github.com/trailheadapps/lwc-recipes)
5. [Lightning Data Service (LDS)](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.data_ui_api): to access data and metadata from Salesforce
6. [Lightning Locker](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.security_locker_service)
7. Lifecycle Hooks:
    - Lightning Web Components provides methods that allow you to “hook” your code up to critical events in a component’s lifecycle. These events include when a component is:
        * Created
        * Added to the DOM
        * Rendered in the browser
        * Encountering errors
        * Removed from the DOM


8. Decorators:
    - @api: Marks a field as public. Public properties define the API for a component.
    - @track: Tells the framework to observe changes to the properties of an object or to the elements of an array.
    - @wire: Gives you an easy way to get and bind data from a Salesforce org.
    
9. a LWC component contain:
    1. .js-meta.xml
    2. HTML file
    3. CSS file
    4. JS file
10. **isExposed **( true or false) makes the component available from other namespaces

References:
[reactivity](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.reactivity)
[Lightning Web Components Dev Guide](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.reference)

- [ ] https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics/handle-events-in-lightning-web-components?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential
- [ ] https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics/add-styles-and-data-to-a-lightning-web-component?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential
---
---

[Salesforce Certified JavaScript Developer I Exam Guide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-JavaScript-Developer-I-Exam-Guide)
notes:

