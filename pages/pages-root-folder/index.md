---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#

####
#
####
layout: simplefront

#header:
#  image_fullwidth: header_unsplash_12.jpg

widget1:
  title: 'ARCTIC Program'
  url: '/about'
  image: ONR-logo-300x.jpg
  text: 'The Alaska Regional Collaboration Innovation and Commercialization (ARCTIC) Program is an Office of Naval Research (ONR) initiative.'
####
#
####
widget2:
  title: "Partners"
  url: '/partners/'
  text: 'Learn more about current activities and programs....'
  video: '<a href="#" data-reveal-id="videoModal"><img src="https://img.youtube.com/vi/90n9ga3SOQQ/0.jpg" width="302" height="182" alt=""/></a>'
####
#
####
widget3:
  title: "Upcoming Events"
  url: '/roadmap'
  image: widget-github-303x182.jpg
  text: 'ARCTIC Program roadmap'

# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://tinyletter.com/arctic-program
  text: Inform me about new updates and features ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

### The Alaska Regional Collaboration for Technology Innovation and Commercialization (ARCTIC) is a collaboration designed to promote commerce and partnerships between Alaska and the Arctic and Pacific regions through advancements in energy through resiliency research, technology development/deployment and education.
{: .text-center}



<hr>

## [Participating Partners](/partners)
{: .text-center }

<div class="row t30">
{% for partner in site.partners %}

<div class="medium-4 columns" markdown="block">
[ ![{{partner.name}} logo]({{partner.logo}}){: .aligncenter } ]({{partner.website}})
_{{partner.tagline}}_
{: .text-center }

</div>
{% endfor %}
</div><!-- /.row -->

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/90n9ga3SOQQ" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
