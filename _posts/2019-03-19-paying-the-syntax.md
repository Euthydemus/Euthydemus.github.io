---
layout: post
title:  "Paying the Syntax"
date:   2019-03-19 23:00:06 -0700
categories: jekyll update
this_is_yaml: "I yam what I yam."
some_boolean: true
string_to_abuse: "The Quick Brown Fox"
some_array:
 - item1
 - item2
 - item3
 - item4
complex_array:
  - name: "foo"
    value: "Four score"
  - name: "bar"
    value: "-7 years"
---

<p>This page exists soley to start recording syntax, because it's weird. At least compared to everything else I know.</p>

<p>I'm also testing partial HTML beyond mere Markdown.\</p>

<p>Let's have a conditional that evaluates to true and loop through an array:</p>
{% if page.some_boolean %}
<ul>
    <li>We don't care right now, but for loops have a .length property.</li>
    {% for val in page.some_array %}
    <li>{{ val }} -- index counts up, rindex counts down: {{ forloop.index }}, {{ forloop.rindex }} -- but cycle flows through a different set: {% cycle "a", "z" %} </li>
    {% endfor %}
</ul>
{% else %}
<p>We could have used elsif, but it's just a boolean.</p>
{% endif %}

<p>"break" can pop loops, obvs.</p>
<p>Less obviously: a for loop can have an else clause to handle null/empty collections.</p>
<p>but this is a trip: "for x in site.y <em>reversed limit: 3 offset: 3</em>" -- that's a 2nd page of 3, starting from the bottom.</p>

<ul>
{% for objs in page.complex_array %}
<li>{{ objs.name }}: {{ objs.value}}</li>
{% endfor %}
</ul>
<p>Note: a null ref didn't break anything; there was a typo above using "obs" instead of "objs"</p>
<p>This is liquid, calling on YAML: {{ page.this_is_yaml }}</p>
<p>Variables set on the layout are also available: {{ layout.big_var }}</p>

<p><a href="https://learn.cloudcannon.com/jekyll-cheat-sheet/">The Cheat Sheet.</a></p>

<h3>Controls</h3>
<ul>
<li>1 == 1</li>
<li>1 != 2</li>
<li>"food" contains "foo"</li>
<li>2 > 1</li>
<li>unless (NOTE: instead of a typical not)</li>
<li>case [variable]... and then each "when [value]" in subsequent blocks, no breaks, closes with endcase</li>
</ul>

<h3>String Abuse (it's |ing hot!, :, params)</h3>
<ul>
<li>Replace: {{ page.string_to_abuse | replace: "Brown", "Red" }}</li>
<li>Size: {{ page.string_to_abuse | size }}</li>
<li>number_of_words: {{ page.string_to_abuse | number_of_words }}</li>
<li>slice: {{ page.string_to_abuse | slice: 4, 10 }}</li>
<li>truncate: {{ page.string_to_abuse | truncate: 10 }}</li>
<li>truncatewords: {{ page.string_to_abuse | truncatewords: 3 }}</li>
<li>split and jsonify: {{ page.string_to_abuse | split: " " | jsonify }}</li>
</ul>

<p>Most of this won't be useful when going for a blog, but the data blocks (cards! Cards! <em>Caaarrrdddsss!</em>)
are very exciting to me.</p>