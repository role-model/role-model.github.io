---
layout: page
description: This page describes the whole project.
---

<img src="img/role_logo.png" alt="drawing" width="150"/>


## Recent News

<!-- Posts -->
<ul id="posts">

	{% for post in site.posts limit:3 %}

	  <li class="post">
	  	<h3><a href="{% if site.baseurl == "/" %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">{%if post.header %}{{ post.header }}{% else %}{{ post.title }}{% endif %}</a></h3><time datetime="{{ post.date | date_to_xmlschema }}" class="by-line"> <i>{{ post.date | date_to_string }}</i> </time>
	  	<span>{{ post.content | strip_html | truncatewords:50 }}</span>
	  </li>

    {% endfor %}

</ul>


#### Head to the News tab for more!
