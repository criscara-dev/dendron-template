---
id: bdf0d0a4-e383-4d9b-8d12-7c79a9645919
title: JavaScript Developer 1
desc: ''
updated: 1611226105920
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

[Lightning Web Components for Aura Developers ](https://trailhead.salesforce.com/content/learn/modules/lightning-web-components-for-aura-developers?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)


Lightning Web Components is an implementation of the W3C’s Web Components standards.

> ⚠️
Important
✅ allowed Aura components can contain Lightning web components.
❌ not allowed Lightning web components can’t contain Aura components.


Aura | LWC
---|---
.cpm starting with `<aura:component>` |.html file starting with: `<template>` and can have nested `<template>` 
attributes: `<aura:attribute>` | ...become JS props `@api recordId; property;...`
Basic Aura Expressions | ...Become HTML Expressions
Migrate `<aura:if>` tags in an Aura component to <br> `<aura:if isTrue="{!v.property.Broker__c}">` | `if:true` or `if:false` directives in a Lightning web component’s HTML file <br> `<template if:true={property.data}>`
Complex Aura Expressions <br> `<aura:if isTrue="{!v.page > 1}">` | ...Become JavaScript Logic <br> `<template if:false={isFirstPage}>`
Aura Iterations <br> `<aura:iteration items="{!v.properties}" var="property">` | ...Become HTML Iterations <br> `<template for:each={properties.data.records} for:item="property">`
Aura Initializers <br> `<aura:handler name="init" value="{!this}" action="{!c.onInit}" />` | ... Become Lifecycle Hooks `connectedCallback()`
Aura CSS <br> Remove the proprietary `THIS`<br> `java.THIS .lower-third {` class that Aura components use. | ...Becomes Standard CSS
Lightning Web Components Inherit Aura Component Styling | &nbsp;

<details><summary>
Migrating a component from Aura to LWC
</summary>

This Aura component uses the lightning:formattedNumber base component.
```java
<aura:component>
    <lightning:formattedNumber value="5000" style="currency"
      currencyCode="USD" />
</aura:component>
```
To migrate this markup to a Lightning web component:

* Change the colon that separates the namespace (`lightning`) and component name (`formattedNumber`) to a dash.
* Change the camel-case component name (`formattedNumber`) to a dash-separated name (formatted-number).
* Change the camel-case attribute name (`currencyCode`) to a dash-separated name (`currency-code`).
Here’s the equivalent Lightning web component.

```java
<template>
    <lightning-formatted-number value="5000" style="currency"
      currency-code="USD">
    </lightning-formatted-number>
</template>
```
</details>

> 💯
The main takeaway is that Lightning web components use standard JavaScript modules

==Use Third-Party JavaScript Libraries==
> To use a third-party JavaScript library in an Aura component or a Lightning web component, you must upload the library as a static resource.

Aura | LWC
-|-
`<ltng:require>` such as <br> `<ltng:require scripts="{!$Resource.resourceName}" afterScriptsLoaded="{!c.afterScriptsLoaded}" />`| ...become `import resourceName from '@salesforce/resourceUrl/resourceName';`
In an Aura component, you can dynamically create a component in JavaScript using $A.createComponent(). | There’s no equivalent for dynamically creating a component in a Lightning web component.
2 ways data binding | 1 way data binding (check below)


<details><summary>
How do you access an ES6 module in Aura component?
</summary>

e added an `aura:id` so that we can get a reference to the module in JavaScript code.
</details>

Ref.
[Use 3rd party JS Lib](https://developer.salesforce.com/docs/component-library/documentation/lwc/lwc.create_third_party_library)

> ⚠️ Use the Wire Service to Get Data
To read Salesforce data, Lightning web components use a reactive wire service, which is built on Lightning Data Service. Components use @wire in their JavaScript class to read data from one of the wire adapters in the lightning/ui*Api namespace. For the list of wire adapters that Salesforce provides, see the Resources section of this unit. You can’t write your own custom wire adapters.

> ⚠️ Important - Use JavaScript API Methods to Write Data
Don’t use @wire to create, update, or delete a record. The wire service delegates control flow to the Lightning Web Components engine. Delegating control is great for read operations, but it isn’t great for create, update, and delete operations. As a developer, you want complete control over operations that change data. That’s why you perform create, update, and delete operations with a JavaScript API instead of with the wire service.

> Use Apex for Custom Data Access

> Use the Wire Service to Call an Apex Method:
- If an Apex method is cacheable (it doesn’t mutate data), you can invoke it from a component via the wire service. You must annotate the method with @AuraEnabled(cacheable=true)

> Call an Apex Method Directly
- If an Apex method mutates (creates, updates, or deletes) data and therefore isn’t cacheable, you must call the method directly in code.

> ⚠️ Note
Don’t `@wire` an Apex method that creates, updates, or deletes data.

> ⚠️  Work with External APIs
Working with external APIs in a Lightning web component is similar to Aura components. By default, you can’t make calls to third-party APIs from JavaScript code in Lightning web components. Add a remote site as a CSP Trusted Site to allow JavaScript component code to load assets from and make API requests to that site’s domain.

> ⚠️  Aura Component Data Binding
- Aura components can use two forms of expression syntax for data binding: {!expr} or {#expr}. We won’t go into the differences here, but let’s look at a simple example.
In Aura components, this data binding is two way. Changes to the `fName` attribute are passed into the child component’s `firstName` attribute, and changes in the value of the `firstName` attribute in the child component are passed back to the `fName` attribute of the owner component. This bidirectional data binding can be expensive for performance, and can create hard-to-debug errors due to the propagation of data changes, especially if you have deeply nested components
- Lightning Web Component Data Binding:
The data-binding behavior is intentionally simpler and more predictable in Lightning web components. The child component must treat any property values passed from the owner component as read-only. If the child component changes a value passed from an owner component, you see an error in the browser console.

To trigger a mutation for the property value provided by the owner component, the child component can send an event to the parent. If the parent owns the data, the parent can change the property value, which propagates down to the child component via the one-way data binding.

Aura | LWC
-|-
Instead of the proprietary `Event` object in Aura components | use the `Event` or `CustomEvent` standard DOM interfaces, as a pub-sub (publish-subscribe) pattern |
`event.fire()`| `this.dispatchEvent(myEvent)`
handle event with `<aura:handler> ` | ... become `<c-child onnotification={handleNotification}></c-child>` note the use of `on`

<details><summary>
What the Application Events Become a Publish-Subscribe Pattern?
</summary>

To have:The pubsub module exports three methods.

- **register**
Registers a callback for an event.
- **unregister**
Unregisters a callback for an event.
- **fire**
Fires an event to listeners.


</details>

<details><summary>
What does a component event in Aura map to in a Lightning web component?
</summary>
to web-standard DOM events in Lightning web components. 
</details>

<details><summary>
What prefix does an Aura handler add to the event name of a Lightning web component?
</summary>
**Lorem ipsum dolor sit amet...**
</details>


---
---

[Salesforce Certified JavaScript Developer I Exam Guide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-JavaScript-Developer-I-Exam-Guide)
notes:

