---
layout: post
title:  "Let's Cut Cards"
date:   2019-03-20 18:30:06 -0700
categories: jekyll update
---

This is a simple post to test the pulling of cards from a data file into a page.
We'll just start with some simple axioms. This will get gussied up later.

{% for law in site.data.axioms %}
<blockquote>
{{ law.text }}
<br>
(<a href="{{ law.xref }}">{{ law.xref }}</a>)
</blockquote>
{% endfor %}