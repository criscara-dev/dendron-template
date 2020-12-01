---
id: 6a84eef0-cbab-4213-aac4-cf6eba6713e9
title: Nonprofit-cloud
desc: ''
updated: 1606852315131
created: 1606729073072
---

## Non Profit Cloud Basics

[Trail](https://trailhead.salesforce.com/content/learn/modules/nonprofit-cloud-basics)
NPSP
![](/assets/images/2020-11-30-09-47-55.png)

[Manage Fundraising, Programs, and Engagement](https://trailhead.salesforce.com/en/content/learn/modules/nonprofit-cloud-basics/relationships-matter-people-and-data) info in this trail.

---

More details from those [trails](https://trailhead.salesforce.com/content/learn/modules/nonprofit-success-pack-basics).

- [Navigate](https://trailhead.salesforce.com/content/learn/modules/nonprofit-success-pack-basics/navigate-nonprofit-success-pack-npsp) and moving around the NPSP App trail

- The main App in NPSP is... NPSP App.

- how the data is organized into NPSP? which are the keys objects and their functions?

- Salesforce [NPSP Glossary](https://docs.google.com/spreadsheets/d/1IRdiWTtBqy0zgCe1KfV2gls7swrrvDaN3UQs9bKcbYs/edit#gid=1164494008) by SF.

[Settings customization](https://trailhead.salesforce.com/content/learn/modules/nonprofit-success-pack-basics/customize-your-settings-in-npsp) trail in NPSP

---

2020-12-01 16:38

- [x] prepare web to Lead in my dev org and create form to embed in my WP website
- create a custom App
- add custom fields to Lead Stnd Obj 

- COMPANY DONATION: Fields needed for Company donation:
step 1: firstname, lastname, email, phone, location
step 2: 
how many desktops?
how many laptops?
how many monitors?
Any other equipment or comments?
How did you hear about the Turing Trust?
* Online search eg. Google
* Social media
* At an event eg. a conference
* Word of mouth
* Other: ______

==Schedule a call back?== may need more work as some sort of processes

I will create just a couples of custom fields to demo:
1. how did you hear...sicne is a checkbox and see how is working
2. how many laptops since is a normal text/number field
![](/assets/images/2020-12-01-19-30-40.png)

- [x] embed form into my WP website
- [x] fill up form and check my org
- [x] is working: the form arrived

==ISSUE need to make a multiselect?! on other...==

- INDIVIDUAL DONATION: fields needed for Individual donations:

Extra fields
- PCs - Please tell us the approximate number of desktops and / or laptops you are donating

==crazy mental==
I think they need to simplify the forms;
1. tell first what you're accepting and excluding a priori what is not up to your standard
ex. Unfortunately...We don't accept those:
- OS (Operative Systems): Linux and other Unix-like (BSD etc.)
- 
2. I'm still trying to do something but need to use picklists with multiselects, I mean:
basically custom picklist (controlling) -> to custom multi-select picklist (dependent)
![](/assets/images/2020-12-01-19-08-27.png)
which computer do you want to donate?
- laptops
- desktops
- tablets/phones

for each then:
- age acceptable:
3 y
3/30 y
>10 y
dont know (actually don't acceptable?)
- OS... select acceptable
Windows 7
...
MacOS 10
...
Android xxx
IOS xxx

- other accessories
HD
RAM
USB
monitors
...

- firstname, lastname, email, phone, location
- How did you hear about the Turing Trust?
* Online search eg. Google
* Social media
* At an event eg. a conference
* Word of mouth
* Other: ______

#### basically on the Lead Object I created 2 new fields:
ex.
1. Device types (as controlled) checkbox
2. OS type (as dependent) multi-picklists
how to link them now?

- maybe 2 business processes/2 page layouts?! 

