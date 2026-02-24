---
status:
region:
due_date:
opr_id: "<% tp.file.title.substring(4) %>"
created: "<% tp.date.now("Do MMM YYYY [at ]HH[hrs & ]mm[min]") %>"
type: operation
---
> [!question] Properties
> `Status` `INPUT[inlineSelect(option(not started), option(started), option(end), option(paused)):status]` `Due Date` `INPUT[datePicker:due_date]` `Region` `INPUT[inlineSelect(option(academic), option(career), option(entertainment), option(finance), option(health), option(knowledge), option(lifestyle), option(relationship), option(skill), option(social), option(spirituality)):region]`
# Overview

> [!danger] **Overdue Tasks**
> ```tasks
> status.type is TODO OR status.type is IN_PROGRESS
> path includes {{query.file.path}}
> due before today
> group by due
> ```

> [!todo] **Today's Tasks**
> ```tasks
> status.type is TODO OR status.type is IN_PROGRESS
> path includes {{query.file.path}}
> due today
> short mode
> ```

> [!calendar] **Upcoming This Week**
> ```tasks
> status.type is TODO OR status.type is IN_PROGRESS
> path includes {{query.file.path}}
> due after today
> due on or before in one week
> group by due
> ```

> [!success] **Completed Tasks**
> ```tasks
> status.type is DONE OR status.type is CANCELLED
> path includes {{query.file.path}}
> group by status.name
> ```
# Task
- [ ] <% tp.file.cursor() %>
# Wiki
```meta-bind-button
label: Create Linked Wiki
icon: "book-plus"
style: plain
class: wiki
actions:
  - type: command
    command: quickadd:choice:a0847609-be65-4fbd-95bc-5a50233dbd01
```

```dataview
TABLE WITHOUT ID 
  file.link AS "Wiki",
  region AS "Region",
  due_at AS "Due At"
FROM "Reflections/Wikis"
WHERE opr_id = this.opr_id
```
