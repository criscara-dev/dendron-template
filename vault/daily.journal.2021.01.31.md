---
id: 6d46fd8f-8feb-487c-9b25-d5f3806046f2
title: '2021-01-31'
desc: ''
updated: 1612116500290
created: 1612082996808
---

Ref: [JS I cert](https://trailhead.salesforce.com/en/users/strailhead/trailmixes/prepare-for-your-salesforce-javascript-developer-i-credential)

## Should do:

- [x] shortcut on MAC to full screen CMD+CTRL+F)
- [webcomponents](https://github.com/WICG/webcomponents)
- [x] [review L dsign system](https://trailhead.salesforce.com/content/learn/modules/lightning_design_system?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)

tomorrow:
- [ ] Vlocity VPE3
- [ ] review: [Lightning Web Components for Visualforce Developers](https://trailhead.salesforce.com/content/learn/modules/lwc-for-visualforce-developers?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
- [ ] [challenge 4 LWC Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge_lwc_specialist?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-javascript-developer-i-credential)
- [ ] [React Udemy](https://www.udemy.com/course/react-for-the-rest-of-us/learn/lecture/17797254#overview)

future:
- [ ] [LWC trail](https://trailhead.salesforce.com/en/content/learn/trails/build-lightning-web-components)
- [ ] [GitHub trail](https://trailhead.salesforce.com/en/content/learn/trails/set-up-your-workspace-and-install-developer-tools)
- [ ] [Flow trail](https://trailhead.salesforce.com/en/content/learn/trails/build-flows-with-flow-builder)

---
Limbo Issues :
- [ ] to create Issue tracker SF:
[today's issue solved](https://trailblazers.salesforce.com/answers?id=9063A000000E5zSQAS): reset password to auth everytime the org...
[another issue](https://trailblazers.salesforce.com/answers?id=9064S000000DIGiQAO): as picture below
![](/assets/images/2021-01-18-12-54-05.png)
issue: cannot authorize org:
1. sfdx force:org:list --all   ... and get the USERNAME of the org you want to use 
2. sfdx force:auth:web:login -a <you-org-name>

2021-01-22 22:10 ISSUE: [Deploy the LWC Recipes App](https://trailhead.salesforce.com/content/learn/projects/quick-start-lwc-recipes-app/deploy-and-get-to-know-the-lwc-recipes-app) I could not add Permission set via CLI so... I did it manually for _recipes_ App on my user.

issue on setting vscode:
cannot add default sintax for react:
```
"files.associations":{
      "*.js":"javascriptreact"    
  }
```
---