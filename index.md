---
layout: default
title: "Βιογραφικό"
---

# {{ site.data.cv.name }}
**{{ site.data.cv.title }}**

📧 [{{ site.data.cv.email }}](mailto:{{ site.data.cv.email }}) · {{ site.data.cv.phone }}

🔗 [GitHub]({{ site.data.cv.links.github }}) · [LinkedIn]({{ site.data.cv.links.linkedin }})

---

## Περίληψη
{{ site.data.cv.summary }}

## Σπουδές
{% for ed in site.data.cv.education %}
- **{{ ed.degree }}**, {{ ed.institution }} ({{ ed.period }})
{% endfor %}

## Εμπειρία
{% for ex in site.data.cv.experience %}
### {{ ex.role }} , {{ ex.org }} , {{ ex.period }}
{% if ex.bullets %}{% for b in ex.bullets %}- {{ b }}
{% endfor %}{% endif %}
{% endfor %}

## Δεξιότητες
{% for s in site.data.cv.skills %}
- {{ s }}
{% endfor %}

## Γλώσσες
{% for l in site.data.cv.languages %}
- {{ l }}
{% endfor %}

[Κατέβασε PDF](./resume.pdf)
