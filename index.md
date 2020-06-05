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
      {% if post.categories.size > 0 %}
      •
      {% for cat in post.categories %}
        <a class="post-cat" href="{{ site.url }}/categories/#{{ cat }}">{{ cat }}</a>
        {% unless forloop.last %}
        <span>/</span>
        {% endunless %}
      {% endfor %}
      {% endif %}
    </p>
    <h4>
      <a href="{{ site.url }}{{ post.url }}" class="post-title" title="{{ post.title | escape }}">{{ post.title }}</a>
      {% if post.link %}
      <a class="post-title-link" href="{{ post.link }}" target="_blank" title="{{ post.title | escape }}"><i class="fa fa-external-link"></i></a>
      {% endif %}
    </h4>

    {% if post.author %}
      {% assign author = site.data.authors[post.author] %}
    {% else %}
      {% assign author = site.owner %}
    {% endif %}

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

      {% if post.image.credit %}
      <span class="image-credit">Photo Credit: <a href="{{ post.image.creditlink }}">{{ post.image.credit }}</a></span>
      {% endif %}
    </div><!-- /.image-wrap -->
    {% endif %}

</section>
{% endfor %}

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
