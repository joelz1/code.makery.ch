---
layout: article
title: "More HTML & CSS: JavaScript with Bootstrap"
date: 2015-04-09 00:00
slug: more-html-css/javascript-bootstrap
github: https://github.com/marcojakob/code.makery.ch/edit/master/collections/library/more-html-css-en-javascript-bootstrap.md
description: "Learn how to integrate the Bootstrap JavaScript into your web page. Contains an example for a Bootstrap navigation."
published: true
prettify: true
comments: true
sidebars:
- header: Articles in this Series
  body:
  - text: "Introduction"
    link: /library/more-html-css/
    paging: Intro
  - text: "Website Layout with Bootstrap"
    link: /library/more-html-css/website-layout/
    paging: 1
    icon-css: fa fa-fw fa-th-large
  - text: "Icons"
    link: /library/more-html-css/icons/
    paging: 2
    icon-css: fa fa-fw fa-flag
  - text: "Images with Bootstrap"
    link: /library/more-html-css/image-bootstrap/
    icon-css: fa fa-fw fa-image
    paging: 3
  - text: "Image Editing"
    link: /library/more-html-css/image-editing/
    icon-css: fa fa-fw fa-image
    paging: 4
  - text: "Free Image Sources"
    link: /library/more-html-css/image-sources/
    icon-css: fa fa-fw fa-image
    paging: 5
  - text: "Formatting Text"
    link: /library/more-html-css/text/
    paging: 6
    icon-css: fa fa-fw fa-font
  - text: "JavaScript with Bootstrap"
    link: /library/more-html-css/javascript-bootstrap/
    paging: 7
    icon-css: fa fa-fw fa-code
    active: true
- header: Links
  body:
  - text: HTML & CSS Tutorial
    link: /library/html-css/
    icon-css: fa fa-fw fa-external-link
languages:
  header: Languages
  collection: library
  item: more-html-css
  part: javascript-bootstrap
  active: en
---

The Bootstrap core is its CSS. However, there is also a JavaScript file that is very useful. Have a look at the [Bootstrap JavaScript page](http://getbootstrap.com/javascript/) to find out what's possible.

In [HTML & CSS Tutorial - Part 7](/library/html-css/part7/), we have seen how the Bootstrap CSS can be integrated. Now, we also want to use the JavaScript file.


## Integrating the Bootstrap JavaScript

While the Bootstrap CSS is always inserted into the `head` area, the JavaScript comes at the very end of the `body` section. The Bootstrap JavaScript also depends on another JavaScript, called *jQuery*. So, our HTML looks like this:

##### HTML Template for Bootstrap

<pre class="prettyprint lang-html">
&lt;!DOCTYPE html>
&lt;html>
  &lt;head>
    &lt;meta charset="utf-8">
    &lt;meta name="viewport" content="width=device-width, initial-scale=1">
    <mark>&lt;link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css"></mark>
    &lt;link rel="stylesheet" href="main.css">
    &lt;title>Bootstrap Template&lt;/title>
  &lt;/head>
  &lt;body>
    &lt;h1>Hello, world!&lt;/h1>

    <mark>&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js">&lt;/script></mark>
    <mark>&lt;script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js">&lt;/script></mark>
  &lt;/body>
&lt;/html>
</pre>

Three things are needed:

* Bootstrap CSS in the `head`.
* jQuery JavaScript at the end of `body`.
* Bootstrap JavaScript at the end of `body`.

*Check the [Bootstrap Website](http://getbootstrap.com/getting-started/) to get the latest version numbers of Bootstrap and jQuery.*


<div class="alert alert-info">
  **Note:** The JavaScript could also be included in the `head` area, but this is not optimal. The browser loads the website step-by-step from top to bottom. When the JavaScript comes too early, this could slow down the loading of the entire web page. That's why it is usually better to have the JavaScript at the very end.
</div>


## Collapsing Navigation

With only the Bootstrap CSS we were already able to program a pretty decent navigation in our Part 7 of our [HTML & CSS Tutorial](/library/html-css/part7#navigation-with-bootstrap). Now we further improve this navigation so that it automatically collapses on small screens.

![Navigation collapsed](/assets/library/more-html-css/javascript-bootstrap/navigation-collapsed.png)

The HTML code looks like this:

<pre class="prettyprint lang-html">
&lt;!DOCTYPE html>

&lt;html>
  &lt;head>
    &lt;meta charset="utf-8">
    &lt;meta name="viewport" content="width=device-width, initial-scale=1">
    &lt;link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css">
    &lt;link rel="stylesheet" href="main.css">
    &lt;title>Portfolio Marco&lt;/title>
  &lt;/head>
  &lt;body>
    &lt;div class="navbar navbar-default navbar-static-top">
      &lt;div class="container">
        
        &lt;div class="navbar-header">
          &lt;button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#my-navbar">
            &lt;span class="sr-only">Toggle Navigation&lt;/span>
            &lt;span class="icon-bar">&lt;/span>
            &lt;span class="icon-bar">&lt;/span>
            &lt;span class="icon-bar">&lt;/span>
          &lt;/button>
          &lt;a class="navbar-brand" href="#">Portfolio Marco&lt;/a>
        &lt;/div>
        
        &lt;div class="collapse navbar-collapse" id="my-navbar">
          &lt;ul class="nav navbar-nav">
            &lt;li class="active">&lt;a href="./">Home&lt;/a>&lt;/li>
            &lt;li>&lt;a href="blog/">Blog&lt;/a>&lt;/li>
            &lt;li>&lt;a href="projects/">Projects&lt;/a>&lt;/li>
            &lt;li>&lt;a href="contact/">Contact&lt;/a>&lt;/li>
          &lt;/ul>
        &lt;/div>
      &lt;/div>
    &lt;/div>
    
    &lt;div class="container">
      &lt;h1 class="title">Welcome to my Portfolio&lt;/h1>
    &lt;/div>
    
    &lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js">&lt;/script>
    &lt;script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js">&lt;/script>
  &lt;/body>
&lt;/html>
</pre>



