---
id: 78b1e12c-8d6a-4912-8eed-6c20e08c7841
title: Apex
desc: ''
updated: 1605097141114
created: 1602930717556
stub: false
---
# Apex

## Commands

| command | what for |
|:--|:--|
| sfdx --help | help 
| sfdx help force | help
| sfdx force:project:create -n project-name | create a new project
| sfdx force:org:create -s -f config/project-scratch-def.json -a alias | create a new scratch org with an alias
| sfdx force:org:list | list all the org and scratch org
| sfdx force:auth:logout -u alias or org-name | disconnect a org
| sfdx force:source:open -u alias | open the newly create org
| sfdx force:org:open | open the component already created
| sfdx force:source:pull | I create a component from setup then in terminal in vscode I can pull in the component...
| sfdx force:source:push | I add some text / html to the component just created in Aura folder and from terminal I can push the changes
| sfdx force:org:delete -u nameScratchOrg | delete a scratch org
| code $HOME/sfdx/sfdx.log | to see log |


consider:
Use "log level parameter for specifying log levels. error = error 
warn = error + warn 
info = error + warn + info 
trace = error + warn + info + trace 
fatal = error + warn + info + trace + fatal

## Apex definitions
- Apex is Salesforce’s cloud-based, object-oriented programming language, specifically designed for customizing and extending apps on the Salesforce platform.

<details><summary>
In which forms Apex exist?
</summary>

Apex can be written in 2 forms: as a #class or a [[ trigger|computer-science.lang.apex.trigger]] (execution is triggered during processing DML statements);
</details>
