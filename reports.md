---
layout: default
title: reports
header: case reports
---
<header>
	<h2>Reports</h2>
</header>

These case reports give you insight into the kinds of vulnerabilities we found, the numbers and how we helped to fix them. mostely they are a summery of our blogposts on our Security Hotline. 

{% assign pages = site.pages |reverse %}
{% for p in pages %}
{% if p.url contains "/reports/" and p.url != page.url %}
<hr>
### [{{ p.Report DIVD-2020-00001: Widespread Citrix Vulnerability }}]({{p.2020-000001-Widespread-Citrix-Vulnerability.md}})
*{{ p.13 March 2020 }}, by {{ p.Chris van 't Hof | default: "anonymous" }}*

{{ p.excerpt }}

[Read more]({{p.url}})
{% endif %}
{% endfor %}
