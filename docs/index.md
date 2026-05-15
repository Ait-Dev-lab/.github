---
layout: default
---

# 📚 Research Documentation

Welcome to the Ait-Dev-lab research documentation. Our work focuses on making LLMs run efficiently in browsers using WebGPU.

---

## 🔬 Research Papers

{% assign papers_by_status = site.research | group_by: "status" %}

{% for status_group in papers_by_status %}
### {{ status_group.name }}

| Title | Description | Date |
|-------|-------------|------|
{% for paper in status_group.items %} | [{{ paper.title }}]({{ paper.url }}) | {{ paper.description }} | {{ paper.date | date: "%b %d, %Y" }} |
{% endfor %}
{% endfor %}

---

## 🚀 Active Projects

| Project | Status | Links |
|---------|--------|-------|
| Stream LLM | ✅ Live | [Demo](https://ait-dev-lab.github.io/stream-llm/) · [GitHub](https://github.com/Ait-Dev-lab/stream-llm) |

---

## 🔗 Quick Links

- [Home](https://ait-dev-lab.github.io/.github/)
- [Live Demo](https://ait-dev-lab.github.io/stream-llm/)
- [GitHub Organization](https://github.com/Ait-Dev-lab)
- [Stream LLM Repository](https://github.com/Ait-Dev-lab/stream-llm)

---

*Documentation auto-updates when new papers are added.*
