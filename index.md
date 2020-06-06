---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in site.posts %}
<a href="{{ post.url }}"><img src="{{ post.thumbnail }}" width="150" height="150"></a>
<div style="color: #40c1dd; text-align: left; font-size: 20px">{{post.date | date: '%Y, %b %d'}}</div>
<div style="text-align: left; font-size: 30px; font-weight: bold"><a href="{{ post.url }}">{{ post.title }}</a></div><br>
{{ post.excerpt }}

<hr>

{% endfor %}

{% for post in paginator.posts %}
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      Previous
    </a>
  {% else %}
    <span class="previous">Previous</span>
  {% endif %}
  <span class="page_number ">
    Page: {{ paginator.page }} of {{ paginator.total_pages }}
  </span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}
    <span class="next ">Next</span>
  {% endif %}
</div>
