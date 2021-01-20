---
id: bdf0d0a4-e383-4d9b-8d12-7c79a9645919
title: JavaScript Developer 1
desc: ''
updated: 1611146742325
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

<details><summary>
How to use the @wire service?
</summary>

```javascript
import { adapterId } from 'adapter-module';
@wire(adapterId, adapterConfig)
propertyOrFunction;
```
adapterId (Identifier)—The identifier of the wire adapter.
adapter-module (String)—The identifier of the module that contains the wire adapter function.
adapterConfig (Object)—A configuration object specific to the wire adapter.
propertyOrFunction—A private property or function that receives the stream of data from the wire service. If a property is decorated with @wire, the results are returned to the property’s data property or error property. If a function is decorated with @wire, the results are returned in an object with a data property and an error property.

---
</details>

    
9. a LWC component contain:
    1. .js-meta.xml
    2. HTML file
    3. CSS file
    4. JS file
10. **isExposed **( true or false) makes the component available from other namespaces

11. Handle Events in Lightning Web Components
![](/assets/images/2021-01-20-09-11-31.png)

Events Up, Properties Down
![](/assets/images/2021-01-20-09-14-11.png)

1. **Passing Information Up**
Information can be passed up using **events** ([CustomEvents](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent)) and **event listeners**.
2. **Passing Information Down**
Information can be passed down using **public properties** and **public methods**.
(Public properties are great solutions for passing down primitive values, simple objects, and arrays.)

> TIP To communicate down the component containment hierarchy, pass properties to the child via HTML attributes, or call its public methods. To communicate between components, use Lightning message service or a publish-subcribe utility.
        
References:
[reactivity](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.reactivity)
[Lightning Web Components Dev Guide](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.reference)

- [ ] https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics/handle-events-in-lightning-web-components?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential
- [ ] https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-basics/add-styles-and-data-to-a-lightning-web-component?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential
---

[Lightning Web Components for Visualforce Developers](https://trailhead.salesforce.com/content/learn/modules/lwc-for-visualforce-developers?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)

- Pre-requisites: [Learn to work with the JS](https://trailhead.salesforce.com/en/content/learn/trails/learn-to-work-with-javascript)
- [Mobile App customization](https://trailhead.salesforce.com/content/learn/modules/salesforce1_mobile_app)
- [webcomponents](https://github.com/WICG/webcomponents)

Low-code | Pro-code
---------|---------
Lightning pages | Lightning Web Components 
Quick actions | Aura Components
URL buttons | Visualforce
Utility bar |
Flows |

Traditional Visualforce Requests | Lightning Web Component Requests
---------------------------------|---------------------------------
![](/assets/images/2021-01-20-09-58-10.png) | ![](/assets/images/2021-01-20-09-58-53.png)
User requests a page. | User requests a component.
The server executes the page’s underlying code and sends the resulting HTML to the browser. | The component definition is returned to the client as a compiled JavaScript file.
The browser displays the page. | The JavaScript application generates the UI.
When the user interacts with the page again, the cycle repeats from step one. | When the user interacts with the page again, the JavaScript modifies the UI on the client.

[Use template directive to conditional rendering](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.create_conditional)

rendering Lists

Visualforce | LWC
--- | ---
<apex:repeat> | for:each and iterator:iteratorName

Invoking JS
```javascript
// eventHandler.html
<template>
    <a onclick={handleButtonClick}></a>
    
</template>
// eventHandler.js
import { LightningElement } from 'lwc';
export default class EventHandler extends LightningElement {
    handleButtonClick(event) {
        // Do whatever...
    }
}
```
[Visualforce Standard Components and
Base Lightning Web Components Side by Side](./assets/pdfs/EquivalentsReference.pdf)

Traditional Visualforce Data Access | Lightning Web Components Data Access
--- | ---
![](/assets/images/2021-01-20-11-36-22.png) | ![](/assets/images/2021-01-20-11-36-42.png)
Visualforce pages that retrieve or modify data use a standard controller or an Apex controller. Traditionally, the client invokes controller methods when the page loads or as actions. After a method runs, the Visualforce engine generates the final markup and sends it to the client. | Lightning web components that retrieve or modify data use Lightning Data Service or Apex methods. The client uses JavaScript to call Lightning Data Service or an Apex method. After Lightning Data Service or an Apex method runs, the Lightning Web Components engine returns the minimal needed data to the client. JavaScript on the client processes the data and generates the final markup.

- [Lightning Data Service](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.data_ui_api) is the preferred (and easiest) way to work with Salesforce data in Lightning web components.
Lightning Data Service is a similar concept to a Visualforce standard controller.

> Note
To use Lightning Data Service, you have two options: Use a base component that allows you to build forms, or use an LDS wire adapter or function. The code to use Lightning Data Service is very specific, and fully explained in Use Lightning Data Service to Work with Data in the Lightning Web Components and Salesforce Data module.

> Apex in LWC
Methods are stateless.
Methods must be @AuraEnabled, and can be marked as cacheable.
You import Apex methods and then call them.
You bind components to record pages in a metadata xml file, and access the record Id in the JavaScript file.
Proper error handling involves throwing exceptions, instead of using page messages.


View State:

Server State | Stateless Methods
---|---
Visualforce uses the view state to maintain state between server requests |  In Lightning web components, server requests are stateless.

Calling Apex:

 in Visualforce | Lightning Web Components
---|---
binding the controller and referencing the Apex methods in the page <apex:page> |  import the methods into the JS file and then invoke the methods in JS:<br> `import queryAccounts from '@salesforce/apex/AccountListControllerLwc.queryAccounts;`


Accessing a Record Id:

 in Visualforce | Lightning Web Components
---|---
retrieve the record Id from the `ApexPages.StandardController` | accessing a record Id in Apex is a little less straightforward
 &nbsp; | Expose the component so that it’s available on record pages.
&nbsp; |In JavaScript, declare recordId as a public property. The parent component (the record Flexipage) populates the value of the recordId property.
Pass the recordId as a parameter in Apex method calls.

Server Errors in Visualforce | Lightning Web Components
---|---
<apex:pageMessages> and <apex:pageMessage> to show errors in different ways |  you decide whether to let exceptions propagate or to gain more control over what’s shown to the user by throwing an AuraHandledException or a custom exception. 

VF | LWC
---|---
URLFOR <br> Visualforce pages often use the URLFOR function with `<apex:commandButton>` and `<apex:commandLink>` tags to navigate to pages inside or outside of Salesforce. The Navigation Service eliminates hardcoded URLs by using meaningful `PageReference` objects to perform navigation. If Salesforce changes a specific URL, code that links to it doesn't break. Apex controller methods also facilitate navigation by returning `PageReferences`.| [Lightning Navigation Service](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.use_navigate)



<details><summary>
How ti use the Navigation Service?
</summary>

1. Import the lightning/navigation JavaScript module into the Lightning web component.
2. Make the Lightning web component’s class extend NavigationMixin.
3. Call the Navigate method, passing the page reference of the page you want to navigate to.
</details>

> Note
You can use a Visualforce page within Lightning Experience.
Visualforce and Lightning web components can also coexist on the same page and interact.
Use the [Lightning Components for Visualforce](https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.use_message_channel) JavaScript Library when you want to include a Lightning web component in a specific location on a Visualforce page


---
---

[Salesforce Certified JavaScript Developer I Exam Guide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-JavaScript-Developer-I-Exam-Guide)
notes:

