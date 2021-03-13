---
id: 0b544b48-373b-4938-9dd3-c75cbe8067c2
title: Vlocity
desc: ''
updated: 1615394583280
created: 1611746683478
---


[link pdf](/assets/pdfs/VlocityCertificationProgramGuide.pdf)

Reference: [Trello board](https://trello.com/b/fTeWCQ5f/vlocity)

==Vlocity is a Managed Packager in the AppExchange==

## Master Vlocity Plan:

- [ ] Roadmap ready?
    - [ ] who is going to give me feedback? 
    - [ ] rewards and stakes at place? 
    - [ ] applied Pareto? 
    - [ ] did you chunk down the work you need to do? 
    - [ ]  did you set the Tree roots? (most basic general elements first?)
    - [ ] did you set space repetition?
    - [ ] did you apply interleaving?
- [ ] Workspace ok? 
- [ ] 3 sets Pomodoro tech? (short and intense practice) and uses of senses
- [ ] feeling?
    - [ ] slept well? 
    - [ ] exercise ok? 
    - [ ] brain ok? 
    - [ ] Feeling good, happy?    
    - [ ] dressed properly, professional?   
- [ ] schedule ready? 
- [ ] work music ok? 
- [ ] start!
...
- [ ] feedback (test yourself): 
    - [ ] did you feel a little uncomfortable? (good for push forward, butterfly in stomach feeling)
    - [ ] community? 
    - [ ] self-testing: NOT re-reading YES re-call!
    - [ ] Task 
  



---

Buzzwords: | time to complete
--|--
**Vlocity Platform Foundations (VPF220)** <br> OmniScript, DataRaptor, Integration Procedure, Cards Framework, Calculation Procedures, and Calculation Matrix. | 5 or 6 hours
**Vlocity Platform Essentials (VPE335)** <br> Cards, OmniScripts, Integration Procedures, DataRaptors, Calculation Matrices, Calculation Procedures, Industry Consoles, and Interaction Launchers | 30 hours

## Preparing for the Exam

To be eligible to take the Platform Consultant exam, you must have:

1. Completed the [Vlocity Platform Foundations](https://vlocity-university.litmos.com/?C=2436808) online course. This course will take you approximately 8 hours to complete.
2. Vlocity highly recommends that you perform additional self-study to maximize your chances of passing the exam.

|Topic|Weighting|
|--- |--- |
|Vlocity Digital Interaction Platform - General|15%|
|FlexCards|20%|
|Vlocity OmniScript|25%|
|Vlocity Data Tools|25%|
|Vlocity Industry Consoles|10%|
|Vlocity Industry Process Library|5%|

<details><summary>
Vlocity Digital Interaction Platform
</summary>

* Explain the principles behind the Vlocity solution and Vlocity's alignment with Salesforce
* Describe the layers and the uses of the key components of the Digital Interaction Platform 
* Explain the purpose and benefits of the Vlocity Data model for each industry
</details>
<details><summary>
Flexcards
</summary>

* Explain when you should use FlexCards
* Describe the types of information and actions that are best suited to FlexCards
* Describe the key capabilities of FlexCards
* Describe the FlexCard Designer
* Explain the purpose of FlexCard data sources
* Explain how FlexCards display fields and actions 
* Determine the fields and actions to display on a FlexCard
* Explain how FlexCards display external data (data from outside of Salesforce)
* Explain the purpose of FlexCard flyouts and when to use them
* Explain the purpose of FlexCard states and how a FlexCard's appearance can change based on conditions
</details>
<details><summary>
Vlocity OmniScript
</summary>

* Explain when you should use Vlocity OmniScripts
* Describe the key capabilities of Vlocity OmniScript
* Give examples of the user experience
* Describe the Vlocity OmniScript Designer
* Explain the purpose and capabilities of OmniScript elements, and recognize how they are categorized
* Explain the basic structure of an OmniScript
* Explain how OmniScripts display data and describe the data sources
* List and explain the best practices for designing OmniScripts
</details>
<details><summary>
Vlocity Data Tools
</summary>

* Explain the purpose, key capabilities, and benefits of Integration Procedures
* Describe how Integration Procedures help synthesize data sources for Cards and Layouts
* Describe how you can use Integration Procedures to display external data on a Vlocity Card
* Describe the Vlocity Integration Procedure Designer
* Describe Vlocity DataRaptors and the purpose and capabilities of each DataRaptor type
* Explain how Integration Procedures and DataRaptors get and save data for an OmniScript
* Describe the Vlocity DataRaptor Designer
* Explain the purpose and key capabilities of Calculation Matrices and Calculation Procedures
</details>
<details><summary>
Vlocity Industry Consoles
</summary>

* Describe the advantages of the 360° view for customers
* Explain the functionality of Vlocity custom components that can be used in an industry console
* Explain the purpose and capabilities of the Vlocity Interaction Launcher
</details>
<details><summary>
Vlocity Industry Process Library (VPL)
</summary>

* Explain the advantages of using the Vlocity Industry Process Library
* Describe how to access and use the Vlocity Industry Process Library
</details>

---

### VPE 1
2021-01-28 10:02
Notes:
Exercises levels: 1/2/3 from easy to hard
Where to get assistance: my Group, Vlocity Community, Vlocity Industry Process Library and click on a process component

#### VPE 1-1
<details><summary>
What happens when you add a Vlocity Managed package to your SF Instance?
</summary>
The integration change the UI
</details>
<details><summary>
What the Data Model Enhancements and Extensions bring to the table?
</summary>

Vlocity:
1. enhance existing standard Salesforce objects and fields
2. and/or add additional custom Salesforce objects and fields
</details>
<details><summary>
Does Vlocity support relationship for Contacts?
</summary>

YEs, they can be can be clarified as **family**, and grouped together in a **household**, or as **business relationships**. 
</details>

![](/assets/images/2021-01-28-10-17-46.png)
for Insurance:
![](/assets/images/2021-01-28-10-19-00.png)
Supporting Telecom and Media Needs
![](/assets/images/2021-01-28-10-22-27.png)
Industry applications
- The Vlocity Industry Process Library is a collection of pre-built, industry-specific process components where you customize your business needs without writing code. Process components are organized by industry.
![](/assets/images/2021-01-28-11-01-20.png)

> 
Digital Experience level:
**FlexCards** (a new generation of Vlocity Cards) and Vlocity **OmniScript** are declarative tools that provide rich user interaction experiences that are understandable by humans.(A Vlocity OmniScript is a way for a human to complete a business process.) A sort of SF Flows
Service Management level:
**DataRaptors** and **integration Procedures**.
data from within and outside of Salesforce.
Developer Experience level:
**Vlocity Build Tool** is a CLI open sourced on GitHub
Industry IDX Workbench.

![](/assets/images/2021-01-28-11-19-44.png)

<details><summary>
What is a DataRaptor?
</summary>

* Get and transform data from Salesforce (DataRaptor Extract)
* Transform and save data to Salesforce (DataRaptor Load)
* Transform any data (DataRaptor Transform)
</details>

![](/assets/images/2021-01-28-11-23-38.png)
<details><summary>
What are Integration Procedures?
</summary>

Vlocity Integration Procedures are declarative, **server-side processes** that execute **multiple actions in a single server call**.
</details>

![](/assets/images/2021-01-28-11-27-27.png)
<details><summary>
What are Vlocity Calculation Procedures?
</summary>
They are another important cross-industry tool that allows us to configure complex math procedurally on top of the Salesforce platform.
</details>

<details><summary>
What is Newport Design System?
</summary>

**Newport Design System** is a Vlocity CSS framework tool for designers and web developers to easily restyle all Vlocity components in a single place and generate custom, optimized CSS that can be used in all future pages including non-Vlocity and non-Salesforce pages
</details>

<details><summary>
What is the Installation Assistant?
</summary>

This tool reduces upgrade effort and assists in **adoption of the latest product functionality**.
</details>

VPE 1-2

<details><summary>
Where Vlocity is available?
</summary>

 Vlocity is Accessible through multiple channels (on Any Device and Any Channel)
</details>

![](/assets/images/2021-01-28-13-45-27.png)

<details><summary>
Which Vlocity App for what?
</summary>

The Vlocity **Digital Studio** app contains the Vlocity Designer Tabs for Vlocity **Platform Essentials**. Use the **VU Console** app to build an **industry console**. The other apps are for use in other Vlocity courses.
</details>

> There are three types of components relevant to Vlocity Platform Essentials:
**Starter**: Where you start building.
**Stub**: Returns static JSON test (mock/custom) data in place of live data
**Sample**: For reference. We have prebuilt samples of everything if you're stuck and you want to compare your component to the equivalent sample.

![](/assets/images/2021-01-28-14-14-53.png)

Natively, data in Vlocity is expressed in JSON format as JSON Nodes and Subnodes - A collection of name/value pairs, usually in a hierarchy


![](/assets/images/2021-01-28-14-16-52.png)

---

2021-01-29 10:06
VP 2-0

Concepts:
1. Web Components
2. Shadow DOM

<details><summary>
Which are 4 LWC benefits?
</summary>

* Low Total Cost of Ownership (TCO)
* High Performance (LWC will load up to 300% faster than their predecessors)
* They’re OmniChannel-enabled
* They’re extremely flexible
</details>

In Vlocity, Omniscript or FlexCard is an **LWC control**. 
![](/assets/images/2021-01-29-10-41-17.png)
![](/assets/images/2021-01-29-10-43-05.png)
LWC in Vlocity are extensible

You can deploy Vlocity LWC via:
`dfsx force:source:push`

|File|Description|
|--- |--- |
|HTML (.html)|Required for all Lightning web components that render UI.Optional for service Lightning web components.|
|JavaScript (.js)|Required for all Lightning web components.If the component renders UI, the JS file specifies which HTML file to return if there's more than one.If you extend a component and create your own custom HTML file, you must modify the JS file to return your custom HTML file rather than the base Vlocity HTML file.|
|CSS (.css)|Required only if the component needs custom styles.If it doesn't, the component uses Salesforce Lightning (SLDS) or Newport (NDS) CSS based on your OmniScript configuration.|
|XML Metadata Configuration(js-meta.xml)|Required for all Lightning web components.|

Type of LWC in Vlocity:
![](/assets/images/2021-01-29-11-49-33.png)

* **Base**: Basic components used by the entire Vlocity platform
* **Platform**: Specific to FlexCards and OmniScripts
* **Vertical**: Digital Commerce: Specific to Communications, Media, and Energy


---

2021-02-01 10:45

### Flexcards Overview: VPE 3-0


#### What FlexCard are and what they can do?
**FlexCards summarize contextual information at a glance.**
- Most FlexCards provide this combination of **information** and **actions**.
**FlexCards are the beginning and ending point for customer transactions**
**We can view FlexCards on any device or channel**
**A FlexCard can display data from multiple data sources**
**We build FlexCards quickly using drag and drop elements** (Within OmniStudio)
**FlexCards have a WYSIWYG editor for controlling their layout and style**
**FlexCard Actions are relevant to the context of the card**
- id est (that is), Update Case action opens a second tab for the Update Case Details guided interaction, which is an LWC OmniScript.
**FlexCards are reusable and embeddable in other FlexCards** (a.k.a. Child FlexCards)
**FlexCards display more detail on demand with Flyouts**
- A Flyout is another FlexCard that appears when you click an action on a FlexCard. A Flyout displays:
additional of secondary information
**FlexCards have multiple states that display based on conditions**
- i.e., a _FlexCard state_ determines what the user **can see and do** on the card.
**We can embed a FlexCard inside an OmniScript**
Obviously, the action that start has a visual UI... i.e. a a FlexCard in a LWC OmniScript


#### Which are the building elements currently available in the FlexCard Designer?

Simple UI elements include: | The more advanced UI elements are: 
--|--
Action | Chart
Block | Custom LWC
Field | Datatable
Icon | FlexCard
Image | State
Menu | &nbsp;
Text | &nbsp;
Toggle | &nbsp;
</details>

### FlexCard Designer

Go to the App: Vlocity Digital Studio -> FlexCards
Available area to work with:
- header 
- canvas
- Build Panel (Build, Properties, Style, and Setup Panels)
- Preview
- Publish options (click Activate)
- In-Product Help and Tool Tips: Click `❓` to view detailed documentation about an element in a slide-out help tray

---
2021-02-02 09:53
VPE 3-1

Creating a FlexCard - Using the Data Source Wizard

- [x] Hands-on-challenge: Create a FlexCard for the Account Detail
- [ ] Step 1: New FlexCard (Configure Basic Settings)
    - ![](/assets/images/2021-02-02-10-37-06.png)
- [ ] Step 2: Select Data Source Type (Integration Procedures)
    - ![](/assets/images/2021-02-02-10-15-53.png)
- [ ] Step 3: Select Data Source:
    Input parameters (Input Map) define what variables to pass to the data source
    - ![](/assets/images/add%20picture%20here.png)
- [ ] Step 4: Configure Inputs (Test Parameters and Test Response)
    - ![](/assets/images/2021-02-02-10-47-54.png)
- [ ] Additional FlexCard **Setup** Properties


<details><summary>
Best Practices?
</summary>

FlexCard Names:

Must begin with a letter
Combination of Name and Author must be unique in an org
Only contains underscores and alphanumeric characters, no spaces
Can’t end with an underscore or have two consecutive underscores
Examples:
Name = AccountActive, Author = CustomerSales
Name = AccountClosed, Author = CustomerSales
</details>

#### [Questions I need to be able to answer](https://vlocity-university.litmos.com/course/3108482/module/6580306/Scorm?LPId=104370)

#### [VPE 3-2 Review Questions](https://vlocity-university.litmos.com/course/3108482/module/6580307/Scorm?LPId=104370)

#### VPE 3-3:
* Make a collapsible block
* Clone a FlexCard
* Configure a field to display a date properly
* Push data from a parent FlexCard to a child FlexCard

> Activating FlexCards and Publish Options
Activate a FlexCard to generate a Lightning web component (LWC). Publish an active FlexCard to a Lightning or Community page. Once activated, a FlexCard can't be edited. You must deactivate it, make your changes, then activate it again.

**A flyout** is a type of action that displays additional data in a modal window or popover.

#### [VPE 3-3 Review Questions](https://vlocity-university.litmos.com/course/3108482/module/6580308/Scorm?LPId=104370)

#### VPE 3-4
Basically I notice the documentation is well organized, how my work should.

make a schema of how I have to proceed.

- Review:
Confirm your understanding by answering these questions.
• What is a benefit of bringing in external data like the Weather to your FlexCard?
-> to help the agent to assess the condition for the intervention...
• How can you pull an image into a card for display?
-> via URL or file upload or... just click the question mark for the tooltip!
• What weather data are you bringing into your FlexCard?
-> The current Condition, temperature and Location/city

Review
Confirm your understanding by answering these questions.
• What is an advantage of using a datatable to display information?
-> see data in a table format
• What is a flyout and how might you use one?
-> It's an `action` it let open another FlexCard/URL from int/ext site to get more date what otherwise will make everything to cluttered
• How do you create a flyout?
From the `properties` of a FlexCard in Action type
• Why might you not be able to view a flyout in a FlexCard?
-> ==because is not set in `action type?==
• Can you embed a child FlexCard in another child FlexCard?
-> Yes
• What is the Repeat Records feature and why must it be disabled for a datatable?
-> in Vlocity, Datatables already loop over list of records.
`Repeat Records` loops as well over list for multiple records, so disable it. 

> Best Practices
BEST PRACTICES
FlexCard state display top to bottom.
The first state that has true conditions displays.
A a best practice, always keep a card state at the bottom that hasn't any conditions. This card becomes the default card state when no conditions are met.

#### [Review Questions VPE 3-4](https://vlocity-university.litmos.com/course/3108482/module/6580310/Scorm?LPId=104370)

#### [Review Questions VPE 3-5](https://vlocity-university.litmos.com/course/3108482/module/6580314/Scorm?LPId=104370)

#### [Review Questions VPE 3-4](https://vlocity-university.litmos.com/course/3108482/module/6580310/Scorm?LPId=104370)

### [FlexCard wrap-up](https://vlocity-university.litmos.com/course/3108482/module/6666592/Scorm?LPId=104370)

---

## VPE-4 Key Capabilities of Vlocity OmniScripts

### VPE 4-0 Overview

<details><summary>
More simple, what is an OmniScript?
</summary>
A way for a person to complete a business process.
3 Steps:
* Get data
* Change Data
* Save Data
</details>

<details><summary>
What is a A Vlocity OmniScript?
</summary>

1. A Vlocity OmniScript is declarative scripting tool that behave as a guided path to complete a business process.
Basically is a way to complete business processes digitally
2. An OmniScript displays both internal data from Salesforce and external data from a website or a 3rd-party legacy system. (AOIs)
3. We rebrand OmniScripts to suit our customers
4. We use OmniScripts to manage signed documents (and we can create dynamic documents with Vlocity from templates)
</details>

<details><summary>
Example of Omniscript?
</summary>
A customer service agent adds a new customer and captures details for a service implementation, such as network configuration requirements
A customer steps through a selling process, such as choosing a new insurance plan
An insurance agent updates a policy
A customer completes a self-service interaction such as troubleshooting a service outage
A customer completes forms for different services, such as government benefits, insurance policies, and healthcare coverage
</details>

![](/assets/images/2021-02-08-12-11-19.png)

<details><summary>
What are OmniOut and CardOut?
</summary>
The capability of hosting OmniScripts and FlexCards on any server is called OmniOut and CardOut.
</details>

### VPE 4-1 Guidelines for Planning OmniScripts

* Map the business process to the proposed OmniScript structure. It's easier to make edits to your process before you begin building.
* Plan what data is involved and where it is needed. This tells you what data must be available for each guided step.
* Decide what data you want to gather and where to save it.

Outline the flow: **Data Process** and **Agent actions**

<details><summary>
What makes each OmniScript unique?
</summary>
Type, Subtype, and Language define the unique identity of the OmniScript
Only one active OmniScript may have the same Type, Subtype, and Language at any time.
The Name is required, but does not have to be unique.
Type must start with a lower case letter.
Use PascalCase...not camelCase
</details>

### [Review VPE 4-1](https://vlocity-university.litmos.com/course/3108510/module/6580384/Scorm?LPId=104370)

---

### VPE 4-2 Getting Salesforce Data for the OmniScript

- When an OmniScript is launched from a Card, the **RecordId** for the card is passed to the OmniScript where it is stored in a variable called **ContextId**.

[VPE 4-2 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580385/Scorm?LPId=104370)
• What are the advantages of using Vlocity Integration Procedures as data sources?
-> They can be versioned, so when updated, you don’t have to change your OmniScript or Card configuration. (e.g. Stub data to live data)
Multiple DataSources (SF, API, Apex) can be combined in one server call.

• Why did you use the same value in the Name and Field Label of the Integration Procedure?
->However best practice when working with LWC is to enter the name in the Field Label. This is because the field label does display in the Action Debugger. Later, when you configure multiple integration procedures, **having descriptive labels** for them helps you confirm if they are pulling and pushing the data correctly.

• What determines the JSON structure of an OmniScript?
-> Aside from the header data, the structure of OmniScript elements determines the JSON structure of an OmniScript.

• How does an OmniScript match incoming data with elements?
-> **OmniScripts have a parser that matches incoming data with the elements based on the element name**. To populate the fields in the UI, you need to change the element names to match the input field names from the Integration Procedure by adding “Account” to the beginning of each element name. 

• Why did we update the mask?
-> Remove the mask as the phone number does not display in a Lightning web component with a mask in place.

---
[VPE 4-3 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580386/Scorm?LPId=104370)
<details><summary>
What are best practices for sending data out of an OmniScript?
</summary>
Use the Action Debugger to get the JSON for Expected Input.
</details>

<details><summary>
What is the merge field syntax for OmniScript? 
</summary>
%node:subnode%
</details>

<details><summary>
What are some uses for the OmniScript Action Debugger? 
</summary>
View the data flow into and out of the OmniScript and copy the JSON to build DataRaptors (which you do in VPE 5).
</details>

<details><summary>
What does a Navigate Action do?
</summary>
Redirects the user to another page or component.
</details>
---

[VPE 4-4 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580387/Scorm?LPId=104370)

<details><summary>
Why shouldn't you let a user edit the Name field?
</summary>
It is read only in Salesforce. Even if you try to update it, no changes will be made.
If you want to let the use edit the name, you can add First Name and Last Name elements, like those in the last block.
</details>

<details><summary>
What are some of the ways you can change the UI of OmniScript elements?
</summary>
Changing the field size with the Control Width slider
Marking a field as Read-only so the user can't manipulate the data
Marking a field as Required so the user must enter data or they can't move forward in the flow
Hiding elements
</details>

<details><summary>
ow is a Salesforce record uniquely identified?
</summary>
The RecordId is a unique identifier for a Salesforce record.
</details>

<details><summary>
What variable identifies the context of an OmniScript?
</summary>
The ContextId variable identifies the context of an OmniScript.
</details>

---

[VPE 4-5 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580389/Scorm?LPId=104370)

<details><summary>
How do you get an element that has a conditional view to populate?
</summary>
Pre-select the most likely path
</details>

<details><summary>
Which OmniScript elements allow users to select from a set of options? What are the differences between them?
</summary>
Radio - one selection as buttons
Select - one selection from dropdown list
Multiselect - one or more selections as checklist
</details>

<details><summary>
What are some best practices for building OmniScripts with conditional views?
</summary>
Minimize them
Use functions to combine logic
Test thoroughly with sad paths 
</details>

---

### VPE 6 Using the Type Ahead Functionality in the UI

When you begin typing, the Type Ahead functionality finds items with similar spelling and displays them in a list. When you choose the contact name you want, the Contact Email for the contact also displays.

[VPE 4-6 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580392/Scorm?LPId=104370)

<details><summary>
What three elements need to be configured for a Type Ahead Block to work?
</summary>
The Type Ahead Block
The Data Element in the Type Ahead Block (e.g. DataRaptor Extract Action)
The Data data source called by the element (e.g. DataRaptor Extract)
</details>

<details><summary>
What three OmniScript elements can be a data source for a Type Ahead Block?
</summary>
DataRaptor Extract Action
HTTP Action
Remote Action
</details>

<details><summary>
Where do you configure what data is displayed in the Type Ahead dropdown?
</summary>
In the Type Ahead Block PROPERTIES in the Typeahead Key Field.
</details>

<details><summary>
What JSON node contains the text that the user types into a Type Ahead Block?
</summary>
The node for the Type Ahead Block in the data JSON.
</details>

<details><summary>
How do you make an element invisible in the UI?
</summary>
Edit as JSON and change the hide node value to true.
</details>

<details><summary>
What are some more ways to change the UI OmniScript Elements
</summary>
Configure the Type Ahead Block edit button and edit mode.
</details>


### VPE 4-7 Validation Data and Handling errors

#### The SAD path

> The idea here is de-activate the `IP` do that we have no more data and we can see if the real data is not coming through once added, what this can means in terms of issues on the App.

[VPE 4-7 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580393/Scorm?LPId=104370)

<details><summary>
What is a requirement for a step to have error checking?
</summary>
At least one element checked as required
</details>

<details><summary>
What is a “Sad path”? In this exercise, how did you simulate one?
</summary>
A "Sad path" is a path where something is wrong in the process. In this case, it can be simulated by deactivating the Integration Procedure Action.
</details>

<details><summary>
What options are there for creating complex logical conditions in an OmniScript?
</summary>
Use multiple Conditions for each element. You must build them several times and take a performance hit. 
Use an equation to evaluate the logic once and then use that element for Conditions. This minimizes conditions. 
</details>

<details><summary>
What are advantages and disadvantages for each?
</summary>
Use multiple Conditions for each element. You must build them several times and take a performance hit. This is good if you only have to evaluate the complex logic once.
Use an equation to evaluate the logic once and then use that element for Conditions. This minimizes conditions. It is good if the same logic needs to be evaluated many times.
</details>

<details><summary>
What settings are required for a Set Errors Element?
</summary>
Conditional View
Element Error Map
Instructional text to the Value field
</details>


### VPE 4-8 Adding external data to an Omniscript

[VPE 4-8 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580395/Scorm?LPId=104370)

<details><summary>
What are examples of external data that a service agent could find useful?
</summary>
Billing data from an onsite database
Weather data
Order tracking information from an order management system
Mapping or other geolocation information
</details>

<details><summary>
What is the merge field syntax for JSON sub nodes in OmniScripts?
</summary>
%node|1:array%, basically from here( %parent|n:node% )
</details>

<details><summary>
Which OmniScript element is basically a rich-text formatted HTML code block?
</summary>
A Text Block
</details>

### VPE 4-9 Adding a warning Banner to an Omniscript

Use merge field syntax to display JSON data in the message text: %Current:Condition%

[VPE 4-10 Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580398/Scorm?LPId=104370)

<details><summary>
Which OmniScript element do you use to add a warning banner?
</summary>
Messaging Element
</details>

<details><summary>
Which types/colors of notification banner are available for the OmniScript?
</summary>
Blue, green, yellow, and red
</details>

<details><summary>
What is special about the Requirement message type? Why do you need to be careful when using it?
</summary>
It makes the element required and enforces error checking
</details>

---

### VPE 4-10 Launching an Omniscript with a Vlocity Action

[Review Questions](https://vlocity-university.litmos.com/course/3108510/module/6580399/Scorm?LPId=104370)

<details><summary>
What is a Vlocity Action?
</summary>
A Vlocity Action is a configurable way to launch a URL including an OmniScript.
</details>

<details><summary>
Can you deploy an Action if it is not active? 
</summary>
No. If an Action isn't active, it can't be deployed.
</details>

<details><summary>
Why did you not use the full URL? 
</summary>
You didn't use the full URL so the action would work in a different org. The full URL would always try to launch in the custom My Domain.
</details>

---

### VPE 4-11 Adding an Interaction Launcher to a Console

==Purpose of  this lesson, is to add an Interaction Launcher to a Console toolbar==

There're 3 types of Interaction Launchers:
- class based;
- object-based;
- OmniScript-based;

<details><summary>
What is the Customer Interaction? What can it be used for?
</summary>
To add the Interaction Launcher as a Utility Item on your Console toolbar, start in Setup and locate the App Manager using Quick Find.
</details>

### VPE-5 Integration procedure

Integration procedures are optimal when:

* You need to access and transform data from third-party sources
* No user interaction is required
* Moving the workload from client to server is preferable

![](/assets/images/2021-02-19-10-06-05.png)
![](/assets/images/2021-02-19-10-14-15.png)
![](/assets/images/2021-02-19-10-15-27.png)
![](/assets/images/2021-02-19-11-25-29.png)

- Explore the Vlocity Integration Procedure Designer
All blocks have one property in common: Execution Conditional Formula. If this formula evaluates to true or is not defined, the block is executed. If it evaluates to false, the block is skipped. 

<details><summary>
What is a Vlocity DataRaptors in a Nutshell?
</summary>
Vlocity DataRaptor is a configurable service for retrieving, transforming, and updating data. Depending on the DataRaptor type, it's a way to:

Get and transform data from Salesforce (DataRaptor Extract)
Transform and save data to Salesforce (DataRaptor Load)
Transform any data (DataRaptor Transform)
</details>

![](/assets/images/2021-02-19-11-40-06.png)

<details><summary>
What are DataRaptor Formulas and Functions?
</summary>
Formulas
A DataRaptor Formula element might contain a formula to:

Perform mathematical operations on numbers.
String together (concatenate) text by using algebraic operators like = + - * / < > and ^.

Functions
A function is an equation you use for operations to:

Manipulate data about date and time
String text together
Determine a result based on logic
Perform mathematical operations

Here are the types of functions available:

Numerical: +, -, *, /, ^, ROUND
Aggregate: SUM, AVG, MAX, and MIN 
Logical: OR, AND and IF.
Example: If the customer's age is less than 18 years old, return a value of "Minor". Otherwise, return a value of "Adult". To make this functionality work, the function would be: IF(AGE<18, "Minor", "Adult").
String: Concatenate
Example: Display city and state together, separated by a comma.
Date and time: AGE, AGEON, DATEDIFF.
Example: TODAY() returns today's date and NOW() returns the current data and time.
</details>

Nmaespaces
-The namespaces in your org will also include the initials of your industry, such as **ins**, **cmt**, and **ps**.

[Object relationship](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/object_relationships)

[What is a Package?](https://trailhead.salesforce.com/en/content/learn/modules/isv_app_development/isv_app_development_packaging)

[Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629059/Scorm?LPId=104370)



1. What does it mean that Vlocity is additive to Salesforce?
- Vlocity either adds additional custom sObjects and fields, or enhances existing, standard sObjects and fields.
2. What offers a visual representation of the sObjects and their links in an org? 
- The [Schema Builder](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/schema_builder).
3. Where can you find a list of sObjects and fields in your org? 
- In the Object Manager.

---

### VPE-5 

[Vlocity Data Model](https://docs.vlocity.com/en/Vlocity-Data-Model.html)

[VPE 5-2 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629060/Scorm?LPId=104370)

<details><summary>
Questions
</summary>

1. What are naming conventions for DataRaptors? 
Requirements:

Name must be unique within the org
Name must have no spaces
Best Practices:

Use prefixVerbObjectDetail in name
Use camelCase
Use an action verb and descriptive nouns
Use abbreviations

2. What type of DataRaptor do you build to pull data from Salesforce? A DataRaptor Extract.

3. What edits did you make to your existing Integration Procedure in this lesson? Removed the Set Values component and added a DR Extract Action component that identified the DR you built. Then changed the response action to send data from the DR Extract Action.
</details>

---

### VPE 5-3 Saving data for the OmniScripts with an Integration Procedure
![](/assets/images/2021-02-22-09-28-51.png)

[5-3 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629062/Scorm?LPId=104370)

1. What did you copy from the OmniScript to create your DataRaptor mappings? We copied the OmniScript JSON with stub data to create the DataRaptor mappings using QuickMatch.

2. What prevents duplicate records in Salesforce in a DataRaptor Load? To ensure you don't create duplicate records in Salesforce when you create your DataRaptor Load, define an Upsert Key.

3. Why did you preview the DataRaptor? Element level testing. Remember that DataRaptor Loads update live data in Salesforce.

---

### VPE 5-4 Getting Primary Contact Data with an Integration Procedure

[5-4 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629063/Scorm?LPId=104370)

1. What two sObjects are used to pull data for the OmniScript in this lesson? The Account and Contact sObjects.

2. What did adding r.FIELDNAME to the end of the field names do? It created a relationship query within your SOQL query.

3. Why did you preview the DataRaptor and your updated OmniScript? To confirm it worked correctly with element level testing.

---

### VPE 5-5 Getting Data for Type Ahead Block

![](/assets/images/2021-02-23-08-39-19.png)
![](/assets/images/2021-02-23-08-39-05.png)

[5-5 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629355/Scorm?LPId=104370)

---

### VPE 5-6 Updating a Primary Contact in a Branching Integration Procedure

[VPE 5-6 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629358/Scorm?LPId=104370)
Why did you go through all three branches before pasting the JSON into the Integration Procedure? To populate the OmniScript JSON with all of the conditional options in order to copy the JSON to help build both the Integration Procedure and DataRaptors.

2. What did you use to identify which DataRaptor should execute? In the integration procedure, a Conditional Execution Formula in each DataRaptor Post Action element.

3. How do you create a new Salesforce record with a DataRaptor Load? Don’t set an upsert key and ensure that you have all the required fields for that record type.

4. What is one example of the power of DataRaptors that you utilized in this exercise? Linking records. The ability to create a record, hold information from that new record (that is a different object type) and use it to link to and update a second record with the same data.

---

### VPE 5-7 getting data for FexCard

![](/assets/images/2021-02-24-09-27-48.png)

[5-7 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629367/Scorm?LPId=104370)

DR -> Account:vlocity_cmt__PrimaryContactId__c
IP -> team/getMasterAccountDetails > Team Starter Get Master Account (Version 1). -> to a new Version: Team Get Master Account
FC -> team > teamMasterAccount (Version 1). -> new version: 


1. What is a benefit of using an Integration Procedure? It allows you to combine different data sources and transform data. The Integration Procedure is versioned to update it without updating the calling tool.

2. How do you recognize a Node in the JSON? There is a colon after the Node name.

3. Why is the order of Extract Steps in a DataRaptor important? Any step that references data from another step must be after that step. For example, the PriContact Step in the teamGetMasterAccountDetails DataRaptor.

4. Where did you preview the Integration Procedure? You previewed the Integration Procedure response in the Card Designer. But you could also have previewed it the Integration Procedure Designer. Try out element level testing whenever possible because it makes troubleshooting easier.

Challenge Exercise VPE 5-7.1: Update the PriContact Extract Path

---


### VPE 5-8 Extracting External Data with an Integration Procedure

![](/assets/images/2021-02-24-11-30-11.png)

[5-8 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629371/Scorm?LPId=104370)



1. What are ways to use weather data in your own project? Think about how weather affects your customers.

2. How do you build your API Return URL? Enter the appropriate parameters into the weatherbit.io Swagger site.

3. What Integration Procedure elements do you use to incorporate external data? Set Values to save the API key and 1 HTTP Action (or 2 if you did the challenge).

==last bit==
You will need a second input; call this input Days.
This is what the Integration OmniScript and Card Layout send to this Integration Procedure.
(Hint: don’t forget your Response JSON Path) ???? what I need to do?s

---

### VPE 5-9 Using a DataRaptor Transform in a Integration Procedure

[5-9 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629373/Scorm?LPId=104370)

1. What does a DataRaptor Transform allow you to do? It allows you to map and transform from one JSON to another. It can also transform XML and custom data schema.

2. How did you update the way the City and State display in the results? used the concatenate formula.

3. What does the Response Action do? It sends the data back to the FlexCard/OmniScript.

---

### vPE 5-10 Testing the count Console End to end

No review qwestion


### VPE 5-11 Building Calculation Matrix


[5-10 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629412/Scorm?LPId=104370)

1. What is a Calculation Matrix? A Calculation Matrix is a lookup table.

2. What are some uses for a Calculation Matrix? 

Insurance premiums matching characteristics of insured to premiums
Age, gender and smoking status for life insurance
Driver age and driving record for an auto insurance policy
Weather alert matrix based on weather conditions 
Demographic data based on a location (such as wages) 
Pricing matrices (like the one created)

3. Can you have multiple Inputs or Outputs to your data? You can have multiple input columns and the combination of inputs for each row must be unique. You can have multiple output columns and none of the elements need to be unique.

4. If two matrices are both enabled at the same time, which one will be called? The one with the highest priority with 1 as the lowest priority.

---

### VPE 5-12

[5-11 Review Questions](https://vlocity-university.litmos.com/course/3108512/module/6629420/Scorm?LPId=104370)

1. What does a Calculation Procedure do in Vlocity? Take inputs as formatted JSON data, use lookup matrices, algebraic operations, and aggregation operations to calculate new data, and output specified data in formatted JSON.

2. What are the two different options for a Calculation step in a Calculation Procedure? Calculation and Matrix Lookup.

3. What is important about the input JSON? It must be on a node called input (with a lower case i).

4. If two Calculation Procedures are both active at the same time, which one will be called? The one with the highest priority with the number 1 as the lowest priority.

5. Where can you get the expected input and output JSON from a Calculation Procedure? From the simulation.



