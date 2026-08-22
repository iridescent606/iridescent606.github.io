---
layout: default
title: 我的博客
---

# 📚 我的博客

欢迎来到我的个人博客，这里记录我的学习和思考。

## 📝 最新文章

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})
📅 {{ post.date | date: "%Y年%m月%d日" }}
{% if post.categories %}
🏷️ {{ post.categories | join: "、" }}
{% endif %}

{{ post.excerpt | strip_html | truncate: 100 }}

[阅读全文 →]({{ post.url }})

---
{% endfor %}

## 🔗 快速链接
- [关于我](/about)
- [所有文章](/blog)
- [联系方式](/contact)
