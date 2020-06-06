---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in site.posts %}
<img src="{{ post.thumbnail }}" width="150" height="150">
{{post.date | date: '%Y, %b %d'}}
<a href="{{ post.url }}">{{ post.title }}</a>
{{ post.excerpt }}
{% endfor %}
