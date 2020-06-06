---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in site.posts %}
        <a href="{{ post.url }}" ><img src="{{ site.baseurl }}/img/{{ post.image }}" width="150" height="150" /></a>
        <h2><a href="{{post.url | prepend: site.baseurl}}" >{{ post.title }}</a></h2>
{{ post.excerpt }}<br>
{{post.date | date: '%Y, %b %d'}} &nbsp; | &nbsp;
{% endfor %}
