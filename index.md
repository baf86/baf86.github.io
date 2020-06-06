---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in paginator.posts %}

<a name="top"><img src="{{ post.thumbnail }}" width="150" height="150"></a>
<h2><a href="{{post.url | prepend: site.baseurl}}">{{post.title}}</a></h2>
{{ post.excerpt }}<br>
{{post.date | date: '%Y, %b %d'}} &nbsp; | &nbsp;
{% capture words %}{{ post.content | number_of_words }}{% endcapture %}{% unless words contains "-" %}{{ words | plus: 250 | divided_by: 250 | append: " minute read" }}

{% endunless %}
{% endfor %}

<hr>

<img src="/img/readmore.gif" width="50" height="50" alt="Read More"><div style="text-align: center; font-size: 30px; font-weight: bold;">Go to More Posts</div>
<!-- Pagination links -->
<div style="text-align: center; font-weight: bold italic;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">Previous</a> &nbsp;
  {% else %}

  {% endif %}
    Page: {{ paginator.page }} of {{ paginator.total_pages }}
  {% if paginator.next_page %}
     &nbsp; <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}

  {% endif %}
</div>
  <br>
   <div style="text-align: center; font-size: 30px; font-weight: bold;"><a href="https://elyserobinson.com/archives">Go to A List of Posts (Archives)</a>
</div>
