---
layout: page
title: InTouch
tagline: Welcome to our Humble Abode
---


<div id="posts">
	{% for post in site.posts limit: 3 %}
		<br/>
		<p>
			<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
			<h3><span class="date">{{ post.date | date_to_string }}</span></h3>
			<div class="content">{{ post.content }}</div>
			<div class="footer"> 
				<div class="tags">
					{% for tag in post.tags %}
						<a class="tag" href="/tags.html#{{ tag }}">#{{ tag }}</a>
					{% endfor %}
				</div>
			</div>
		</p>
	{% endfor %}
</div>
