---
layout: default
title: reports
header: reports
---
<header>
	<h2>Not a regular office</h2>
</header>

These reports give you insight into the kinds of vulnerabilities we find in general and how to fix them. Findings on specific organisations are only published after vulnerabilities are fixed and in negotiation with the stakeholders involved. We are not journalists, we only try to make the internet safer.

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
