time:: <%tp.file.creation_date('HH:mm')%>

# <% tp.date.now('YYYY-MM-DD') %>

>[!note]+ daily highlight
>

## notes to review
```dataview
table date, tags, priority
from "01 inbox"
where priority
sort priority desc
```
## todo's
### for today
```tasks
not done
happens today
overdue
filename does not include <%tp.date.now("YYYYMMDD")%>
short mode
hide task count
```
### upcoming
```tasks
not done
scheduled after today OR starts after today
filename does not include <%tp.date.now("YYYYMMDD")%>
short mode
hide task count
```
## today's plan
- [ ] 

## quick capture
jot down random thoughts here...