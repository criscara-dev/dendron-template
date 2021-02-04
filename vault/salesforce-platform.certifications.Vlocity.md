---
id: 0b544b48-373b-4938-9dd3-c75cbe8067c2
title: Vlocity
desc: ''
updated: 1612437859213
created: 1611746683478
---


[link pdf](/assets/pdfs/VlocityCertificationProgramGuide.pdf)

Reference: [Trello board](https://trello.com/b/fTeWCQ5f/vlocity)

==Vlocity is a Managed Packager in the AppExchange==


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