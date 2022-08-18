
This is the index file.

Testing for now.

{% for post in site.posts %}
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p><small><strong>{{ post.date | date: "%B %e, %Y" }}</strong> . {{ post.category }} . <a href="http://myname.github.com{{ post.url }}#disqus_thread"></a></small></p>
{% endfor %}
