<%* tR += "---\n"; %>
<%*
const statusOptions = ["backlog", "reading", "finished"];
const selectedStatus = await tp.system.suggester(statusOptions, statusOptions);
tR += `status: ${selectedStatus}\n`;
%>
template: booknote
created_at: <%* tR += tp.date.now("YYYY-MM-DD HH:mm:ss a"); %>
<%* tR += "\n---"; %>

## 3 Sentence Summary
1. 
2. 
3. 


## Mind Map

<%* 
const title = await tp.system.prompt("Please enter a title.")
const createMM = await tp.system.suggester((item) => item, ["Create a mindmap", "Skip"])
await tp.file.move(`logs/${title}`)

_%>

> [!NOTE] At a glance
> - **Link**: [[<% createMM === "Skip" ? "\\" : `mindmaps/${(await tp.file.create_new(tp.file.find_tfile("templates/mindmap"), `mindmaps/${title}`)).basename}` %>]]
> - (Optional) Generate a mindmap, capture a screenshot, and embed its image here



## Notes




## Discussion Questions



## Links


