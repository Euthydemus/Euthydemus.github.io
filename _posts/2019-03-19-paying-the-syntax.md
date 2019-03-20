---
layout: post
title:  "Paying the Syntax"
date:   2019-03-19 23:00:06 -0700
categories: jekyll update
some_boolean: true
some_array:
 - item1
 - item2
 - item3
---

<p>This page exists soley to start recording syntax, because it's weird. At least compared to everything else I know.</p>

<p>I'm also testing partial HTML beyond mere Markdown.\</p>

<p>Let's have a conditional that evaluates to true and loop through an array:</p>
{% if page.some_boolean %}
<ul>
    {% for val in page.some_array %}
    <li>{{ val }}</li>
    {% endfor %}
</ul>
{% else %}
<p>We could have used elsif, but it's just a boolean.</p>
{% endif %}