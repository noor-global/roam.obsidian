---
region:
aliases:
opr_id:
type: wiki
repeat: spaced every day
due_at: <% tp.date.now("YYYY-MM-DDTHH:mm:ssZ") %>
hidden: true
---
> [!question] Properties
> `Region` `INPUT[inlineSelect(option(academic), option(career), option(entertainment), option(finance), option(health), option(knowledge), option(lifestyle), option(relationship), option(skill), option(social), option(spirituality)):region]` `Next Review` `INPUT[datePicker:due_at]` `INPUT[text(placeholder(Operation)):opr_id]`

<% tp.file.cursor() %>