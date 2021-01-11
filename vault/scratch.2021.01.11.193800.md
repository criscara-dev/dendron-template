---
id: fa357061-92c3-4f0c-8c53-9c5ccbd79894
title: '193800'
desc: ''
updated: 1610393959410
created: 1610393882548
---

Deploy checklist

## Step 1
- [ ] open UAT folder in VSCode to have a vailable the forms
- [ ] open Gform for quick [ref](https://docs.google.com/document/d/1ks86E8l-yFnkIspCwxdtRwBL6DsRnPiKi-zK1d29XoU/edit): 
- [ ] open [GSheet](https://docs.google.com/spreadsheets/d/1GBzyMf1C0Q34LM2nRwvglu5Egh9o7D3kJOxqY1XjOMQ/edit) to check/update IDs: 
- [ ] log into production Org in Firefox: https://um5.lightning.force.com/lightning/page/home and generate:
    - [ ] remove all standard fields
    - [ ] add custom fields as on the right: 
    ![](/assets/images/2021-01-11-19-30-09.png)
- [ ] in Prod Org now I can -> Set Lead Settings as Sandbox to: “keeping the existing record type”
- [ ] go to setup -> Object manager -> Lead -> Record Type -> open both links and get the IDs (15 chard) from the URL and use it to update the form ID in UAT folder.
- [ ] copy over IDs to new forms in UAT named: devsand-business and devsand-individual 
- [ ] add IDs and form ID and record Type for each individual form
 
 ## Step 2
- [ ] open TT website: https://turingtrust.co.uk/wp-admin/edit.php?post_status=publish&post_type=page&paged=2
- [ ] open those links:
    - B: https://turingtrust.co.uk/wp-admin/post.php?post=2669&action=elementor
    - [ ] remove html box and add custom html box with my web-to-lead from UAT folder
    - I: https://turingtrust.co.uk/wp-admin/post.php?post=1048&action=elementor
    - [ ] remove html box and add custom html box with my web-to-lead from UAT folder
    - [ ] add custom JS script "snippet-ID1048.js" and check that the "select" tag has the correct ID from the new generated web-to-lead
 

---

 Final checks:
 - [ ] are forms arrived to SF?
 - [ ] are form arrived with the correct record type?
 - [ ] are the fields filled up?
 - [ ] are the web form redirecting to proper thank-you page? 

  