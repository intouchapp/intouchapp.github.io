---
layout: page
title: InTouch
tagline: Welcome to our Humble Abode
---


<div id="posts">
	{% for post in site.posts limit: 3 %}
		<p>
			<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
			<div class="content">{{ post.content }}</div>
			<div class="footer"> 
				<div class="tags">
					{% for tag in post.tags %}
						<a class="tag" href="/tags.html#{{ tag }}">#{{ tag }}</a>
					{% endfor %}
				</div>
				<span class="date">{{ post.date | date_to_string }}</span><span class="author"> posted by {{ site.author.name }} in</span>
				<span><a class="category" href="/categories.html#{{ post.category }}">{{ post.category }}</a></span>
				<span><a class="comments" href="{{ post.url }}#disqus_thread"></a></span>
			</div>
		</p>
	{% endfor %}
</div>
