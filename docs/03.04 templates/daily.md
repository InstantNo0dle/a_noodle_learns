time:: <%tp.file.creation_date('HH:mm')%>
« [[<% tp.date.now('YYYYMMDD', -1) %>]] | [[<% tp.date.now('YYYYMMDD', +1) %>]] »

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
happens before date(today) OR happens today
filename does not include <%tp.date.now('YYYYMMDD')%>
short mode
hide task count
sort by due
```
- [ ] 
### upcoming
```tasks
not done
happens after today
filename does not include <%tp.date.now("YYYYMMDD")%>
short mode
hide task count
sort by due
```
- [ ] 
## today's plan
- [ ] 

## quick capture
jot down random thoughts here...