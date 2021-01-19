---
id: fa357061-92c3-4f0c-8c53-9c5ccbd79894
title: '193800'
desc: ''
updated: 1610701104875
created: 1610393882548
---

Deploy checklist

## Step 1
- [x] open UAT folder in VSCode to have a vailable the forms
- [x] open Gform for quick [ref](https://docs.google.com/document/d/1ks86E8l-yFnkIspCwxdtRwBL6DsRnPiKi-zK1d29XoU/edit): 
- [x] open [GSheet](https://docs.google.com/spreadsheets/d/1GBzyMf1C0Q34LM2nRwvglu5Egh9o7D3kJOxqY1XjOMQ/edit) to check/update IDs: 
- [x] log into production Org in Firefox: https://um5.lightning.force.com/lightning/page/home and generate:
    - [x] remove all standard fields
    - [x] add custom fields as on the right: 
    ![](/assets/images/2021-01-11-19-30-09.png)
- [x] in Prod Org now I can -> Set Lead Settings as Sandbox to: “keeping the existing record type”
- [x] go to setup -> Object manager -> Lead -> Record Type -> open both links and get the IDs (15 chard) from the URL and use it to update the form ID in UAT folder.
- [x] copy over IDs to new forms in UAT named: devsand-business and devsand-individual 
- [x] add IDs and form ID and record Type for each individual form
 
 ## Step 2
- [x] open TT website: https://turingtrust.co.uk/wp-admin/edit.php?post_status=publish&post_type=page&paged=2
- [x] open those links:
    - B: https://turingtrust.co.uk/wp-admin/post.php?post=2669&action=elementor
    - [x] remove html box and add custom html box with my web-to-lead from UAT folder
    - I: https://turingtrust.co.uk/wp-admin/post.php?post=1048&action=elementor
    - [x] remove html box and add custom html box with my web-to-lead from UAT folder
    - [x] add custom JS script "snippet-ID1048.js" and check that the "select" tag has the correct ID from the new generated web-to-lead
 

---

 Final checks:
 - [ ] are forms arrived to SF?
 - [ ] are form arrived with the correct record type?
 - [ ] are the fields filled up?
 - [ ] are the web form redirecting to proper thank-you page? 

---

2021-01-14 12:37

### Nicola Docs

- Feature requested on 14-01-2021
- Option A Clear all fields in a form upon going back with browser back button = https://stackoverflow.com/questions/8861181/clear-all-fields-in-a-form-upon-going-back-with-browser-back-button
- Option B the quicker and safer implementation is autocomplete="off": https://www.w3schools.com/tags/att_autocomplete.asp

#### DOCS

- Plugins: plugins in WP have not been installed for the purpose of the project;
- Styles (quick linked from logged in):https://turingtrust.co.uk/wp-admin/customize.php?return=%2Fwp-admin%2Fedit.php%3Fs%3Dold%26post_status%3Dpublish%26post_type%3Dpage%26action%3D-1%26m%3D0%26seo_filter%26readability_filter%26paged%3D1%26action2%3D-1

-All changes have been made in Appearance -> Customize -> Custom CSS/JS: from current line 143 to 441 (see far left)

- The JavaScript for Individual form is at the bottom of this section: Appearance -> Customize -> Custom CSS/JS

- New lives URLs:
    1. https://turingtrust.co.uk/give-computers/give-computers-individuals/
    2. https://turingtrust.co.uk/give-computers/business-it-donation-form/

- old Google forms have not been deleted but SAVED with prefix old (as a backups) and currently moved/changed as drafts
    1. https://turingtrust.co.uk/give-computers/old-business-it-donation-form/
    2. https://turingtrust.co.uk/give-computers/old-give-computers-individuals/
 

 ### Neil Docs

- Generate web to lead:
1. Official docs: https://help.salesforce.com/articleView?id=setting_up_web-to-lead.htm&type=5  
2. from Setup: Home -> in [quick search] type: web -> (button) Create Web-to-lead form -> 
- Select from Available fields the ones you want to generate and/or remove the one you don't need; 
- add a Return URL
- de-select reCAPTCHA
- click the button -> Generate

Copy and paste the this HTML form into a text Editor (any but VSCode is preferable)
-Add all necessary styles and if you have:
- record types -> add:
<input id="recordType" name="recordType" type="hidden" value="get this value from record type URL 15 characters" />
- extra info such as Lead Source with predefined valued of web:
<input id="lead_source" name="lead_source" type="hidden" value="Web" />

- where to get record types and what they are (trailheads)
- how to create via code links: https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_link_mailto 

 Trails recommended:
 - Create Reports and Dashboards for Sales and Marketing Managers: https://trailhead.salesforce.com/en/content/learn/projects/create-reports-and-dashboards-for-sales-and-marketing-managers?trail_id=learn-admin-essentials but special this module: 
    - Reports: https://trailhead.salesforce.com/content/learn/projects/quickstart-reports
 - Configure an Email Letterhead and Template: https://trailhead.salesforce.com/en/content/learn/projects/customize-an-org-to-support-a-new-business-unit/configure-an-email-letterhead-and-template?trail_id=learn-admin-essentials
 - All this trail (3 Modules) but a special recommendation for: 
    - Customize a Sales Path (create a Sale Process and Record Type): https://trailhead.salesforce.com/en/content/learn/projects/customize-a-sales-path-for-your-team/customize-a-sales-path?trail_id=learn-admin-essentials
- Customize a Salesforce Object: https://trailhead.salesforce.com/en/content/learn/projects/customize-a-salesforce-object?trail_id=learn-admin-essentials

- Create and Convert Leads: https://trailhead.salesforce.com/content/learn/modules/leads_opportunities_lightning_experience/create-and-convert-leads-lightning?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-administrator-credential
- Work Your Opportunities: https://trailhead.salesforce.com/content/learn/modules/leads_opportunities_lightning_experience/work-your-opportunities?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-administrator-credential