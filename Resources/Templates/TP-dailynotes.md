---
<%*
const title = tp.file.title;
const today = moment(title).format("YYYY-MM-DD");
const yesterday = moment(title).subtract(1, 'days').format("YYYY-MM-DD");
const tomorrow = moment(title).add(1, 'days').format("YYYY-MM-DD");
-%>
created: <% tp.file.creation_date() %>
updated: <% tp.file.creation_date() %>
tag: ['DailyNote']
---

# <% today %>

<< [[<% yesterday %>]] | [[<% tomorrow %>]]>>

![[0000 Index π₯]]

---
### π Daily Questions

##### π μ΄μ ―λ°€μ λ...

- <% tp.file.cursor(0) %>

##### π μ§κΈ λΉμ₯ λ  ν₯λ―Έλ‘­κ² λ§λλ κ²μ...

- 

##### π μ€λ λ΄κ° λ¬μ±νκ³ μ νλ κ²λ€μ...

- [ ] 

##### π μ€λ λμκ² λ₯μΉ μ΄λ €μμ...

- 

---

# π Notes

- 

---

### Notes created today

```dataview
List FROM "" WHERE file.cday = date("<%today%>") SORT file.ctime asc
```

### Notes modified today

```dataview
List FROM "" WHERE file.mday = date("<%today%>") SORT file.mtime asc
```
