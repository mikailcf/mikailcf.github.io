---
layout: page
title: "Post samples"
---

<div class="posts">
  {% for post in site.posts %}
    {% if post.super == null %}
      <div class="post">
        <h2 class="post-title">
          <a href="{{ post.url }}">
            {{ post.title }}
          </a>
        </h2>

        <span class="post-date">{{ post.date | date_to_string }}</span>

        {{ post.content }}
      </div>
    {% endif %}
  {% endfor %}
</div>

<h2 class="page-title">This is the old About page</h2>

<p class="message">
  Hey there! This page is included as an example. Feel free to customize it for your own use upon downloading. Carry on!
</p>

In the novel, *The Strange Case of Dr. Jeykll and Mr. Hyde*, Mr. Poole is Dr. Jekyll's virtuous and loyal butler. Similarly, Poole is an upstanding and effective butler that helps you build Jekyll themes. It's made by [@mdo](https://twitter.com/mdo).

There are currently two themes built on Poole:

* [Hyde](http://hyde.getpoole.com)
* [Lanyon](http://lanyon.getpoole.com)

Learn more and contribute on [GitHub](https://github.com/poole).

## Setup

Some fun facts about the setup of this project include:

* Built for [Jekyll](http://jekyllrb.com)
* Developed on GitHub and hosted for free on [GitHub Pages](https://pages.github.com)
* Coded with [Sublime Text 2](http://sublimetext.com), an amazing code editor
* Designed and developed while listening to music like [Blood Bros Trilogy](https://soundcloud.com/maddecent/sets/blood-bros-series)

Have questions or suggestions? Feel free to [open an issue on GitHub](https://github.com/poole/issues/new) or [ask me on Twitter](https://twitter.com/mdo).

Thanks for reading!