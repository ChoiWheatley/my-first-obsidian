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

![[0000 Index 🔥]]

---
### 📅 Daily Questions

##### 🌜 어젯밤에 난...

- <% tp.file.cursor(0) %>

##### 🙌 지금 당장 날 흥미롭게 만드는 것은...

- 

##### 🚀 오늘 내가 달성하고자 하는 것들은...

- [ ] 

##### 👎 오늘 나에게 닥친 어려움은...

- 

---

# 📝 Notes

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
