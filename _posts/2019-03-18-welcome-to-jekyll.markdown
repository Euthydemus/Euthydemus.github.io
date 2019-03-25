---
layout: post
title:  "What am I even doing?"
date:   2019-03-18 23:00:06 -0700
categories: jekyll update
description: "First post!"
---
So this is me now. I was using WordPress but I'm not willing to go down the path they're going down
and I want to try something different so here we are with a GitHub account to write pages in the
Ruby-based Jekyll. I don't know if it will actually last; the thing that I really wanted here was
broken from the git-go (that's a pun, not a command) and there was some swearing at GitHub before I
discovered that adding + to "git push origin +HEAD:master" will force GitHub to accept a violent
revert.

I'm not looking forward to how brittle, depedency-riddled, and high-maintenance this is going to be, 
especially since it's underpowered with the intention of DIY-ification. I thought I was into that, 
and then I tried integrating some code from 3 years ago.

But I am liking the notion of JSON objects that I can just mesh into my posts (Cards! I will use it
for Cards!) and working more directly with the internals of the beast instead of having the CMS
overriding me with its second-guesses at every turn.

Pay no attention to this next bit.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
