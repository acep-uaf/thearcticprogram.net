---
layout: page
show_meta: true
title: "Ongoing Projects"
subheadline: "Layouts of Feeling Responsive"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/ongoing-projects/"
---

## The ARCTIC project is a technology and education ONR initiative in Alaska.  

The ARCTIC project was modeled off the successful ONR initiative: [Asia-Pacific Technology and Education Partnership (APTEP)](https://www.aptec.net).

> APTEP promotes commerce and partnerships in the Asia-Pacific region through advancements in alternative energy research, technology development and education.


<ul>
    {% for post in site.categories.ongoing %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
