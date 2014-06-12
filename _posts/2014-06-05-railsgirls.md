---
layout: post
title: Rails Girls D.C.
description: "Who Run the World?"
modified: 
category: code
tags: [code]
comments: true
<!-- image:
  feature: texture-feature-05.jpg
  credit: Texture Lovers
  creditlink: http://texturelovers.com -->
---

# Literacy is a right

### And Scandinavians do it better

This post feels like it's going to be a bit of a quilt. Sorry I'm still learning how to anchor tag in liquid/Github pages.

I just did a [lightning talk on civic hacking], to a room full of new dev girls that I've Coached through their first app all day.

You know that moment when you know you're doing the thing you're supposed to be doing?

That. — at Silver Spring Civic Center

<blockquote class="twitter-tweet" lang="en"><p>Got my coach hat (shirt) on :D Ready to help build some first apps today at <a href="https://twitter.com/search?q=%23RGDCworkshop&amp;src=hash">#RGDCworkshop</a> <a href="https://twitter.com/search?q=%23rails&amp;src=hash">#rails</a> <a href="http://t.co/UHliSEYRTC">pic.twitter.com/UHliSEYRTC</a></p>&mdash; Naomi Freeman (@Naomi_Freeman) <a href="https://twitter.com/Naomi_Freeman/statuses/474505257658372096">June 5, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
<script>
function toggle(id){
    var elem = document.getElementById(id);
    if(elem.style.display == 'block'){
        elem.style.display == 'none'
    } else if(elem.style.display == 'none'){
        elem.style.display == 'block'
    }
}
</script>
<input type="button" onClick="hideStuff('themes')" value="Hide">
<input type="button" onClick="showStuff('themes')" value="Show">
<div id="themes" style="display:block">
    <h3>Stuff</h3>

##The Rails Girls Way
<i>from <a href="http://guides.railsgirls.com/guide">Rails Girls Guides</a></i>

###The Basics

Rails Girls events are non-profit. We don’t charge the participants and do not pay for coaches or speakers. Participants don’t need any previous knowledge about programming and there are no age-limitations. All the participants need is a laptop and some curiosity.

The two-day event includes a lot of small group working and short focused talks on programming, design and web. No panel discussions or podium-talks - the spirit should be informal and hands-on. The more you can remove abstractions and add inclusivity the better.

###Rails Girls philosophy

Show sparks, personality and keep in mind the big picture. Explain, repeat and always tie what you’re telling into a larger context.

Internet was made by people and it doesn’t break by a little tinkering. Continuously show the human side: encourage coaches to talk about open source communities, their programming idols and their aspirations.

Copy-pasting rules. Programming per se isn’t central - you can’t really learn to speak Chinese in one day, in a similar manner you can only learn the basic vocabulary and expressions in coding. The goal of every event is to make something visible!

Girls run this world! But also women, ladies, even boys are allowed in. More than semantics we’re interested in a mindset. Both founders were born in the Spice Girls era, they don’t see the word girl as condescending or cutesy-cute.

<hr />

TIL:

- collect will return values and each will not
- creating a rake task will be the easiest way to retrieve emails from a database
(which is important for me right now because the hackathon I'm co-planning, we're about to create a mini site to take in emails for pre-registration, but I hadn't yet worked out how I'd get the emails back out of the database)

<hr />

This is the simplest way I've seen to install Bootstrap in Rails.
I've been in a few hackathons recently where we spent far too much time trying to get Bootstrap in gear. It used to be really strong, but it's been causing more harm than good recently. A configuration used in Rails Girls seems to tame it:

1. {% highlight ruby %} gem install bootstrap-sass {% endhighlight %}
2. In terminal, bundle install
3. in assets - stylehseets - application, add:
{% highlight ruby %} *= require bootstrap {% endhighlight %}

The second advantage - and the reason we did it this way - is that you don't need much internet. With the gem, you're installing it once, and then with this *= require, it's like telling it to link to a stylesheet, which happens to be contained by the gem.

It avoids you needing internet once it's installed, which was important for us, since the internet went down in our room. 
<hr />


The ladies were also introduced to MINASWAN
(Matz is nice and so we are nice)

![Matz]({{ site.url }}/images/yukihiro_matsumoto_bw.jpg)
{: .image-pull-center}

<iframe src="http://embed.ted.com/talks/angela_lee_duckworth_the_key_to_success_grit.html" width="640" height="360" frameborder="0" scrolling="no" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

<blockquote> "...transforms thinkers into creators." </blockquote>
on the table stretching tail flick feed me. Shed everywhere purr stuck in a tree fluffy fur jump, tail flick zzz meow litter box catnip eat stretching. Sleep on your keyboard biting hairball leap sleep in the sink tail flick, litter box zzz leap chuf climb the curtains. Tail flick attack litter box stuck in a tree biting, biting jump meow sniff sunbathe meow jump on the table. Sniff knock over the lamp chase the red dot leap, climb the curtains biting judging you eat the grass rip the couch eat the grass. Lick sunbathe run meow eat, jump I don't like that food biting chuf sniff.
<br />
<blockquote> The worst day of being a programmer is better than my best day at my previous work. </blockquote>
<br />

###More About "What is Rails Girls?"
<iframe width="560" height="315" src="//www.youtube.com/embed/_rkkFdQeBlA" frameborder="0" allowfullscreen></iframe>
<i> With liquid + embed, I can't set this video to a start time. It begins at 1:57. </i>
<br />

term
: definition 1
: definition 2

<hr />
###Contribute
All of the Rails Girls guides are open source and can be contributed to <a href="https://github.com/railsgirls/railsgirls.github.com">here</a>!

### Resources
<h2> Beginner's Guide to Command Line </h2>
 by <a href="https://twitter.com/mad_typist">Jessie Link</a>: 

<script async class="speakerdeck-embed" data-id="9d047860ce1f0131e1db2aa9d004a740" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>

<h2> Ruby in 100 Minutes </h2>
<i>For Ruby/Rails installation, see [here]</i>

<a href="http://tutorials.jumpstartlab.com/projects/ruby_in_100_minutes.html">Go to tutorial</a>

<h2> Workshop Schedule - Rails Girls D.C. 2014 </h2>
<a href="https://docs.google.com/document/d/1LCei7600elHliBVYJdourGZu0V9kSpsFKHzZuo4N5YI/edit" />Schedule
