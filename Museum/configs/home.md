---
type: dashboard
last_update: <% tp.date.now("YYYY-MM-DD HH:mm") %>
---

$$ {\huge {\color{blue}R}.{\color{red}O}.{\color{green}A}.{\color{orange}M}.}$$  
$$ {\large Reflection.Operation.Asset.Museum }$$
$$ {\small {\color{olive}Hello}, \ Muntasir! \ Let's \ work \ on \ something \ great.} $$

> [!tip] At a Glance
> `BUTTON[button-today-journal]` `BUTTON[button-new-op]` `BUTTON[button-new-wiki]`

---

## 📥 Terminal Inbox

> [!danger] **Overdue Inbox**
> ```tasks
> not done
> path includes Operations/Tasks/Others/quick.md
> due before today
> short mode
> ```

> [!todo] **Today's Stream**
> ```tasks
> not done
> path includes Operations/Tasks/Others/quick.md
> due today
> short mode
> ```

> [!calendar] **Pending Processing**
> ```tasks
> not done
> path includes Operations/Tasks/Others/quick.md
> no due date
> limit 10
> short mode
> ```


> [!todo]  **Upcoming Tasks**
> ```tasks
> not done
> due tomorrow or today
> path includes Operations/Tasks
> limit 5
> short mode
> ```

---

## ⚡ Active Operations

```dataview
TABLE WITHOUT ID
  file.link AS "Operation",
  status AS "Status",
  due_date AS "Deadline",
  region AS "Region"
FROM "Operations"
WHERE type = "operation" AND status = "started"
SORT due_date ASC
```

---


### Buttons
```meta-bind-button
label: Open Today's Journal
icon: "calendar-check"
style: primary
id: button-today-journal
actions:
  - type: command
    command: daily-notes
```

```meta-bind-button
label: Create New Operation
icon: plus-circle
style: primary
class: ""
cssStyle: ""
backgroundImage: ""
tooltip: ""
id: button-new-op
hidden: false
actions:
  - type: command
    command: quickadd:choice:1f890d78-5e5c-4cd4-93e9-a78498c54fe3

```

```meta-bind-button
label: Create new Wiki
icon: book-plus
style: primary
class: ""
cssStyle: ""
backgroundImage: ""
tooltip: ""
id: button-new-wiki
hidden: false
actions:
  - type: command
    command: quickadd:choice:a0847609-be65-4fbd-95bc-5a50233dbd01

```
