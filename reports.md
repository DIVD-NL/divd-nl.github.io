---
layout: default
title: reports
header: case reports
---
<header>
	<h2>Reports</h2>
</header>

These case reports give you insight into the kinds of vulnerabilities we found, the numbers and how we helped to fix them. We don't mention specific organisations who were vulnerable, unless they are fine with that. We are not journalists, we only try to make the internet safer.

{% assign pages = site.pages |reverse %}
{% for p in pages %}
{% if p.url contains "/reports/" and p.url != page.url %}
<hr>
### [{{ p.title }}]({{p.url}})
*{{ p.date }}, by {{ p.author | default: "anonymous" }}*

{{ p.excerpt }}

[Read more]({{p.url}})
{% endif %}
{% endfor %}
