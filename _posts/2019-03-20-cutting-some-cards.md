---
layout: post
title:  "Let's Cut Cards"
date:   2019-03-20 18:30:06 -0700
categories: jekyll update
description: "Time to get up to the starting line."
---

This is a simple post to test the pulling of cards from a data file into a page.
We'll just start with some simple axioms. This will get gussied up later.

{% for law_hash in site.data.cards.axioms %}
{% assign law = law_hash[1] %}
<blockquote>
{{ law.text }}
<br>
(<a href="{{ law.xref }}">{{ law.xref }}</a>)
</blockquote>
{% endfor %}

What we really care about is whether or not we can inject cards in here like this:

<blockquote>
<p>{{ site.data.cards.foucault.discipline.cards[0].text }}</p>
<footer>{{ site.data.cards.foucault.discipline.cards[0].cite }}</footer>
</blockquote>

And perhaps also in passing, like when discussing how the name of this blog
means "to teach is to destroy" <label for="sn-to-teach" class="margin-toggle sidenote-number"></label>
<input type="checkbox" id="sn-to-teach" class="margin-toggle"/>
<span class="sidenote">{{ site.data.cards.foucault.willtoknow.cards[0].cite }}</span>
because it's kind of a cool bit of rebranding to finally have a new name
that so explicitly signals on a desire for reinvention, but mostly I just
want to see if I can keep resuable cards and have working sidenotes.

<h3>References</h3>
<p>{{ site.data.cards.foucault.discipline.fullcite }}</p>
<p>{{ site.data.cards.foucault.willtoknow.fullcite }}</p>