---
publish: true
---
## Online 
[[LLM]] 
[[Note Taking]]
[[Podcast Generation]]

## My Tools
[[⭐🤩 Emoji]]

## All Tools
[[🗒NotebookLM]] 
[[🔍 Elicit]] 
[[⭐📚 Obsidian]] 
[[📖 Notion]]
[[🗒NotebookLM]]
[[🔍 Elicit]] 
[[⭐📚 Obsidian]]

```dataview
table collection as Collection, url as "Outbound Link"
FROM "3. RESOURCES/🛠️ Tools"
WHERE collection = "tool"
sort length ASC
```

### By Use Case
```dataview
table without id use as "Use Case", length(rows.file.link) as "Count", rows.file.link as "Tools" 
FROM "3. RESOURCES/🛠️ Tools" 
WHERE uses 
FLATTEN uses as use 
GROUP BY use 
SORT length(rows) DESC
```

### By Tag
```dataview
TABLE length(rows) as "Count", rows.file.link AS Notes
WHERE file.etags
FLATTEN file.etags AS tags
WHERE startswith(tags, "#tools/")
GROUP BY tags AS Tags
SORT tags ASC

```

