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

    {% if post.thumbnail %}
    <div class="post-image-feature">
      <img src=
      {% if post.thumbnail contains 'https' %}
      "{{ post.image.feature }}"
      {% else %}
      "{{ site.url }}/img/{{ post.thumbnail }}"
      {% endif %}
      alt="{{ post.title | escape }} feature image">
</section>
{% endfor %}
