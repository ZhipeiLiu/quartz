---
<%*
let title = tp.file.title;
if (title.startsWith("未命名")){
	title = await tp.system.prompt("新建笔记命名",title);
	if (!title) return;
}
if (title == ""){
	title = "未命名";
} else {
	await tp.file.rename(title);
}
const aTags = ["RC", "investing"];
let tag = await tp.system.suggester(aTags, aTags);
if (tag == "SPT"){
	tag ="RC, SPT";
}
-%>
created: <% tp.file.creation_date() %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
tags: <% [tag] %>
aliases: <% [title] %>
---



#### Follow #todo 
1. [ ] 