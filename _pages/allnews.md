---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

<div class="jumbotron">
{% for article in site.data.news %}
<b>{{ article.date }}</b>

{{ article.headline }}

{{ article.text }}

{% if article.image %}
<a href="#" data-bs-toggle="modal" data-bs-target="#newsModal-{{ forloop.index }}">
<img src='{{ site.url }}{{ site.baseurl }}/images/{{ article.image }}' style='max-height: 80px; max-width: 200px; margin: 1%' alt='{{ article.headline }}'/>
</a>

<!-- Minimal Bootstrap modal -->
<div class="modal fade" id="newsModal-{{ forloop.index }}" tabindex="-1" aria-labelledby="newsModalLabel-{{ forloop.index }}" aria-hidden="true">
<div class="modal-dialog modal-dialog-centered">
<div class="modal-content">
<div class="modal-body text-center p-0">
<img src='{{ site.url }}{{ site.baseurl }}/images/{{ article.image }}' class="img-fluid" alt='{{ article.headline }}'/>
</div>
</div>
</div>
</div>
{% endif %}

{% endfor %}

</div>
