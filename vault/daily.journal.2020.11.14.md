---
id: 43236b17-8175-404b-9a70-7c271d919a17
title: '14'
desc: ''
updated: 1605365297138
created: 1605348317615
---

### To do

- [ ] [review flashcards](https://trailhead.salesforce.com/en/content/learn/trails/platform-app-builder-certification-prep?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-platform-app-builder-credential)
- [x] Node 
- [ ] New Trailhead  
- [x] mermaid flowchart ex.

---

Flocharts in mermaid

 #GANTT
```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```
---
 #Entity-diagram
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```
---
 #Flowchart
```mermaid
graph LR
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```
---

