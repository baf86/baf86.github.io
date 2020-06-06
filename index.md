---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in site.posts %}
<a href="{{ post.url }}"><img src="{{ post.thumbnail }}" width="150" height="150"></a><br>
<div style="color: #40c1dd; text-align: center; font-size: 16px; font-weight: bold">{{post.date | date: '%Y, %b %d'}}</div><br>
<div style="text-align: center; font-size: 18px; font-weight: bold"><a href="{{ post.url }}">{{ post.title }}</a></div><br>
{{ post.excerpt }}
{% endfor %}
