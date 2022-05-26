<%*
let today = tp.date.now ("YYYY-MM-DD") 
let inputDate = await tp.system.prompt("输入示例: "+today, today) 
titleName = window.moment(inputDate, "YYYY-MM-DD", true).format ("YYYY-MM-DD-dddd") 

before_date=window.moment(inputDate,"YYYY-MM-DD",true).add(-1,"days").format("YYYY-MM-DD-dddd") 

after_date=window.moment(inputDate, "YYYY-MM-DD", true).add(1,"days").format("YYYY-MM-DD-dddd") 
-%>
---
created: <% tp.file.creation_date() %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
tags: diary
---
<< [[<% before_date %>]] | [[<% after_date %>]] >>
<% tp.web.daily_quote() %>

<% tp.web.random_picture("200x200", "landscape,water") %>

## Day Planner
- [ ] 9:30 Morning Panel
- [ ] 10:00 
- [ ] 11:00 
- [ ] 12:00 Break
- [ ] 13:30 
- [ ] 14:00 
- [ ] 15:00 
- [ ] 16:00 
- [ ] 17:00 
- [ ] 17:30 Break
- [ ] 20:00 
- [ ] 23:59 End

## Reflections
1. 
2. 
3. 

## Fleeting Notes #todo/tolearn 

