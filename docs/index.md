---
layout: default
title: "Curriculum Vitae"
---

# {{ site.data.cv.name }}
**{{ site.data.cv.title }}**

📧 [{{ site.data.cv.email }}](mailto:{{ site.data.cv.email }}) · {{ site.data.cv.phone }}

🔗 [GitHub]({{ site.data.cv.links.github }}) · [LinkedIn]({{ site.data.cv.links.linkedin }})

---
 
## Summary
{{ site.data.cv.summary }}

## Studies
{% for ed in site.data.cv.education %}
- **{{ ed.degree }}**, {{ ed.institution }} ({{ ed.period }})
{% endfor %}

## Experience
{% for ex in site.data.cv.experience %}
### {{ ex.role }} , {{ ex.org }} , {{ ex.period }}
{% if ex.bullets %}{% for b in ex.bullets %}- {{ b }}
{% endfor %}{% endif %}
{% endfor %}

## Skills
{% for s in site.data.cv.skills %}
- {{ s }}
{% endfor %}

## Languages
{% for l in site.data.cv.languages %}
- {{ l }}
{% endfor %}
