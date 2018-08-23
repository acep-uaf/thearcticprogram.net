---
layout: page
show_meta: false
title: "Participating Partners in ARCTIC"
#subheadline: "An Office of Naval Research initiative"
#teaser: "About the program, project and partners"
#header:
#   image_fullwidth: "header_unsplash_12.jpg"
permalink: "/partners/"
---

<div class="panel radius" markdown="1">
{: #toc }
*  TOC
{:toc}
</div>

{% for partner in site.partners %}

[![{{partner.name}} logo]({{partner.logo}}){: .alignright }]({{partner.website}})
### [{{partner.name}}]({{ partner.website }})

{{partner.teaser}}

_{{partner.tagline}}_

<a class='button secondary' href='{{ partner.website }}' target="#">{{ partner.name }} Website</a>

{{ partner.content }}

{% endfor %}
