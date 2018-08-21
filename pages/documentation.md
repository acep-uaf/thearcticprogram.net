---
layout: page
dayne-note-original-layout: page-fullwidth
title: "ARCTIC Program Resources"
subheadline: "How to use Feeling Responsive"
teaser: "Documentation for ARCTIC website templating system"
permalink: "/documentation/"
#header:
#   image_fullwidth: "header_roadmap_2.jpg"
---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->

<div class="medium-8 medium-pull-4 columns" markdown="1">
{% include _improve_content.html %}

## Getting Started

1. Open `_config.yml` and work it through, it's well documented
1. Add your own `logo.png` to `/assets/img/`.
1. Open `_data/socialmedia.yml` and add your own social media links.
1. Open `_data/navigation.yml` and customize your navigation.
1. Open `_data/language.yml` and translate the theme if necessary.
1. Open `_data/services.yml` and customize links in the footer.
1. Open `_data/network.yml` and customize links in the footer.
1. Open `_data/authors.yml` and edit author information and set default author in `config.yml`.
1. [Read the documentation][1] to check out all features of *Feeling Responsive*.
1. Make it yours and add your own content.

<a class="radius button small" href="{{ site.url }}{{ site.baseurl }}/documentation/">Check out the documentation for all the tricks ›</a>


 [1]: {{ site.url }}{{ site.baseurl }}/documentation/

## Headers

Style your Header!

These are your options to style the header of each webpage individually. <em>Feeling Responsive</em> uses <a href='http://srobbin.com/jquery-plugins/backstretch/'>Backstretch by Scott Robin</a> to expand them from left to right. The width should be 1600 pixel or higher using a ratio like 16:9 or 21:9 or 2:1."

<ul>
    {% for post in site.tags.header %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

## Edit Navigation   {#edit-navigation}

To customize the navigation of *Feeling Responsive*, you have to open the [YAML](https://jekyllrb.com/docs/datafiles/)-file `_data/navigation.yml`. Edit the data and adjust it to your own needs.

## Different Page/Posts Formats   {#formats}

*Feeling Responsive* supports you with different templates for your content. These are the actual page/post formats:

### Page/Post
The [page/post format]({{ site.url }}{{ site.baseurl }}/design/page/) has no sidebar by default, its content is centered and beneath the content the visitor gets some metadata like categories, tags, date and author if provided via data in front matter of the post.

use in front matter via: `layout: page`

### Page/Post with a left or right sidebar
If you want to show the sidebar, just enter `sidebar: left` or `sidebar: right` in front matter, and *whoops, there it is*! To customize the content of the sidebar, open `_includes/sidebar`.


### Page/Post with or without metadata
If you want to show metadata like categories, tags and date at the end of the page, just enter `show_meta: true`. It's on by default. You can change it via `_config.yml`. To turn of metadata just enter – *yes, you guessed right* – `show_meta: false`.



### Page Full Width
If you want full control of styling a page, then use the [page fullwidth template]({{ site.url }}{{ site.baseurl }}/design/page-fullwidth/). To set up a grid, just use the [foundation grid system](http://foundation.zurb.com/docs/components/grid.html).

use in front matter via: `layout: page-fullwidth`


### Frontpage
This template is special. It allows you to define three *widgets* which are displayed with a headline, image, description and a link to the content. It's used for the [homepage]({{ site.url }}{{ site.baseurl }}) of this website.

use in front matter via: `layout: frontpage`


### Video
If you're a video producer or cineast, you'll like the [video template]({{ site.url }}{{ site.baseurl }}/design/video/). It darkens the layout to black and lets the video stand out full-width.

use in front matter via: `layout: video`

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }




## Style your content with   {#styling}

Feeling Responsive offers lots of possibilities to style your articles. You can style your content in different ways. There are elements like subheadlines, feature images, header images, homepage images, meta data like categories and tags and many more.


### subheadlines

If you need a subheadline for an article, just define a subheadline in front matter like this:

`subheadline:  "Subheadline"`

### Quotes

Quotes mix it up a little bit, if you write long articles. So use quotes:

> Age is an issue of mind over matter. If you don't mind, it doesn't matter.
<cite>Mark Twain</cite>

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }


## Comments

You can use comments with *Feeling Responsive* by the way of Disqus. If you want to use Disqus-Comments just open `config.yml` and add your `disqus_shortname`. [More on how to use Disqus ›](https://disqus.com/websites/)

By default comments are turned off. You can customize the default behaviour in `config.yml`. To **turn on comments** just add `comments: true` to front matter using the page layout `layout: page`.

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }




## Responsive Videos

With foundation responsive videos are easy. [More ›](http://foundation.zurb.com/docs/components/flex_video.html)

<div class="flex-video">
        <iframe width="1280" height="720" src="//www.youtube.com/embed/WoHxoz_0ykI" frameborder="0" allowfullscreen></iframe>
</div>

### Code to use for flexible videos

{% highlight html %}
<div class="flex-video">
  <iframe with video />
</div>
{% endhighlight %}


<img class="t60" src="{{ site.urlimg }}header_homepage_13.jpg" alt="">

## Images: Title, Thumbnails, Homepage   {#images}

There are several types of images you can define via front matter. If you want to change the images used in the header have a look at [Style your Header]({{ site.url }}/headers/).


### Title Images

~~~
image:
    title: image.jpg
~~~


### Thumbnails

Thumbnails are used on archive pages like the [blog index][2]. They have a size of 150x150 pixels. Define them in front matter like this:

~~~
image:
    thumb: thumbnail_image.jpg
~~~


### Homepage Image

If you want to feature an article on the homepage with a huge image, then use the homepage image with a width of 970 pixels. If no homepage image is defined *Feeling Responsive* writes instead *New Blog Articles* over the blog entries. Define the homepage image like this:

~~~
image:
    homepage: header_homepage_13.jpg
~~~



### Captions with URL

Sometimes you want to give credit to the creator of your images, maybe with a link. Especially when you use Creative Commons-images like I do for this website. Just add the following front matter and *Feeling Responsive* does the rest:

~~~
image:
    title: header_image.jpg
    caption: Image by Phlow
    caption_url: "http://phlow.de/"
~~~

### Define all images for an article

~~~
image:
    title: title_image.jpg
    thumb: thumbnail_image.jpg
    homepage: header_homepage_13.jpg
    caption: Image by Phlow
    caption_url: "http://phlow.de/"
~~~


<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }


## Create a Table of Contents
{: .t60}

With the Kramdown parser for Markdown you can render a table of contents for your documents. Just insert the following HTML in your post before the actual content. More information on [»Automatic ›Table of Contents‹ Generation«][1].

### Bare Bones Version
{% highlight html %}
### Table of Contents
*  Auto generated table of contents
{:toc}
{% endhighlight %}

### Foundation panel version

{% highlight html %}
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
{% endhighlight %}
<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }

## Breadcrumbs

To turn on breadcrumbs, just use...

{% highlight html %}
breadcrumb: true
{% endhighlight %}


## Includes
{: .t60}

Includes can be very helpful to spice up your content. You can use includes in your Markdown-files with ease: Just call them with some Liquid code.

### list-posts.html

The `list-posts.html`-include is a loop to list posts. It's a helper to add some additional content fast and easy. You can use it in individual posts for example. Which parameters you use, depends on you.

Possible parameter for the loop:

- entries › define the number of entries to show
- offset › define the offset (number of entries to skip before displaying the first one)
- category › define **only one** category to display according entries

The loop looks like this when you use all parameters. Single parameters are possible of course.

~~~
{% raw %}{% include list-posts entries='3' offset='1' category='design' %}{% endraw %}
~~~

### next-previous-post-in-category.html

This include creates a next/previous link to a post of the same category using the first categories-variable in front matter.

~~~
{% raw %} {% include next-previous-post-in-category %}{% endraw %}
~~~


### improve_content

If your content is on Jekyll you can use this include to automatically generate a »Edit on GitHub Link« to give people a possibility to improve your content. Got the idea from [Ben Balters Blog](http://ben.balter.com/).

~~~
{% raw %}{% include _improve_content.html %}{% endraw %}
~~~


### list-collection

This include lets you loop through a collection to list all entries in that collection. If you set »published: false« in front matter of a collection page the page gots filtered out via unless. The following example loops through a collection called *wordpress*.

~~~
{% raw %}{% include list-collection collection='wordpress' %}{% endraw %}
~~~


### alert – Embed an alert in your content

This include lets you easily display an alert. To use the include no `.html` ending is necessary. You can use five different kinds of alerts: `warning`, `info`, `success`, `alert` and `text`.

~~~
{% raw %}{% include alert warning='This is a warning.' %}
{% include alert info='An info box.' %}
{% include alert success='Yeah, you made it!' %}
{% include alert alert='Danger!' %}
{% include alert terminal='jekyll -serve' %}
{% include alert text='Just a note!' %}{% endraw %}
~~~

{% include alert warning='This is a warning.' %}
{% include alert info='An info box.' %}
{% include alert success='Yeah, you made it!' %}
{% include alert alert='Danger!' %}
{% include alert terminal='jekyll -serve' %}
{% include alert text='Just a note!' %}

You can even use `<html>`-tags inside the alert. Beware: Use " and ' properly.

~~~
{% raw %}{% include alert info='<em>Feeling Responsive</em> is listed on <a href="http://jekyllthemes.org/">http://jekyllthemes.org</a>' %}{% endraw %}
~~~

{% include alert info='<em>Feeling Responsive</em> is listed on <a href="http://jekyllthemes.org/">http://jekyllthemes.org</a>' %}

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }


## Javascript/Foundation modules

*Feeling Responsive* uses the foundation framework and some of its javascript components. I reduced the modules, to decrease page load and make the theme faster.

I only added one other javascript-module: [`backstretch`][3] by Scott Robbin. These modules are currently used by the theme and included in `javascript.min.js`. There is also a non-minified version, if you want to take a closer look: `javascript.js`.

~~~
/foundation/bower_components/foundation/js/vendor/jquery.js'
/foundation/bower_components/foundation/js/vendor/fastclick.js'
/foundation/bower_components/foundation/js/foundation.accordion.js'
/foundation/bower_components/foundation/js/foundation.clearing.js'
/foundation/bower_components/foundation/js/foundation.dropdown.js'
/foundation/bower_components/foundation/js/foundation.equalizer.js'
/foundation/bower_components/foundation/js/foundation.magellan.js'
/foundation/bower_components/foundation/js/foundation.topbar.js'
/foundation/js/jquery.backstretch.js'
~~~


## Info about Feeling responsive

 Since years I am programming and designing websites. I love to work with open source tools and learn via code from others. This time I want to try to give something back and learn at the same time.

 *Feeling Responsive* is my first theme which I let into the world. It's built on work and knowledge of others. While I am still designing it, you read about whats behind this theme in the – *hopefully* – near future.


### Features

 * [Responsive Gallery][8], [Videos][9], [Grid][10], [Typography][11],...
 * 100% GitHub Pages friendly
 * Easy editable navigation, footer and social media links
 * Language Ready – just translate one file.
 * Lots of possibilities to customize it to your needs
 * Lots of different headers
 * Various post formats to let your content shine
 * Uses Jekyll 3.0
 * Multiple possibilities to use images in different ways
 * Fine typography
 * Play Video and Audio with [Mediaelement.js][12]

### I got inspired by...

 [Michael Rose][13] and his fabulous [themes for jekyll][14]. Authors of [A List Apart][4] and [Smashing Magazine][5] since 2002. [GitHub][6] and how they built such a habitat for cooperation worldwide. [Automattic][15] and how they built a fantastic community around WordPress. And many, many more...

 Please make *Feeling Responsive* yours and if you like it, please link back to my homebase <a href="http://phlow.de/">Phlow</a>. That would be awesome.

##### Since then, fork it!

 Yours sincerely, [Moritz »mo.« Sauer][7]





  {% include _improve_content.html %}

  </div><!-- /.medium-8.columns -->
  </div><!-- /.row -->

   [1]: http://kramdown.gettalong.org/converter/html.html#toc
   [2]: {{ site.url }}/blog/
   [3]: http://srobbin.com/jquery-plugins/backstretch/
   [4]: http://alistapart.com/
   [5]: http://www.smashingmagazine.com/
   [6]: https://github.com/
   [7]: http://sauer.io
   [8]: {{ site.url }}/design/gallery/
   [9]: {{ site.url }}/design/video/
   [10]: {{ site.url }}/design/grid/
   [11]: {{ site.url }}/design/typography/
   [12]: {{ site.url }}/design/mediaelement_js/
   [13]: http://mademistakes.com/about/
   [14]: http://mademistakes.com/work/jekyll-themes/
   [15]: http://automattic.com/
   [16]: #
   [17]: #
   [18]: #
   [19]: #
   [20]: #
