---
layout: default
---

## About Me

Without a plan, Elyse Y. Robinson moved to Mexico City after her mother passed away from blood cancer. She never heard of Mexico City nor even visited Mexico before. She just knew she had to escape to mourn. She is going into her fourth year here while building <a href="https://www.beaforeigner.com">BeAForeigner Inc.</a>

<hr>

{% for post in site.posts %}
<section class="post">
  <header class="post-header">
    <p class="post-meta">
      <span class="post-date">
        {{ post.date | date: "%-d %b %Y" | upcase }}
      </span>

    </p>
    <h4>
      <a href="{{ site.url }}{{ post.url }}" class="post-title" title="{{ post.title | escape }}">{{ post.title }}</a>
      {% if post.link %}
      <a class="post-title-link" href="{{ post.link }}" target="_blank" title="{{ post.title | escape }}"><i class="fa fa-external-link"></i></a>
      {% endif %}
    </h4>
    </header>

    {% if post.excerpt %}
    <div class="post-description">
      <p>
        {{ post.excerpt }}
      </p>
    </div>
    {% endif %}

    {% if post.image.feature %}
    <div class="post-image-feature">
      <img src=
      {% if post.image.feature contains 'http' %}
      "{{ post.image.feature }}"
      {% else %}
      "{{ site.url }}/img/{{ post.image.feature }}"
      {% endif %}
      alt="{{ post.title | escape }} feature image">
</section>
{% endfor %}

<hr>

{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <p class="author">
    <span class="date">{{ post.date }}</span>
  </p>
  <div class="content">
    {{ post.content }}
  </div>
{% endfor %}

<img src="/img/readmore.gif" width="50" height="50" alt="Read More"><div style="text-align: center; font-size: 30px; font-weight: bold;">Go to More Posts</div>

<!-- Pagination links -->
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      <div style="text-align: center; font-weight: bold italic;">
Previous
    </a> &nbsp;
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
</div>

<br>
<div style="text-align: center; font-size: 30px; font-weight: bold;"><a href="https://elyserobinson.com/archives">Go to A List of Posts (Archives)</a>
</div>
