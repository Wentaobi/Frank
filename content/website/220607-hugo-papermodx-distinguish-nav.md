---
title: "PaperMod 区分列表和文章的导航文字"
date: 2022-06-07
draft: false
isCJKLanguage: true
tags: ["hugo", "paper-modx"]
series: ["PaperModx 定制文章页"]
---

**需求**：PaperMod 列表页面和文章页面的导航文字都是`上一页/下一页`，这在中文表述中不太准确，因此将文章页面的文字改为`上一篇/下一篇`

> 1. 编辑 i18n
---
title: "./i18n/zh.yaml"
---

- id: prev_post
  translation: "上一篇"

- id: next_post
  translation: "下一篇"

> 2. 编辑页面导航模板
```html { title="./layouts/partials/post_nav_links.html" }
{{ i18n "prev_page" }} 改为 {{ i18n "prev_post" }}
{{ i18n "next_page" }} 改为 {{ i18n "next_post" }}
```
