---
layout: home
---
# All Essays

<main class="page-content" aria-label="Content">
    {% assign all_entries = site.posts | concat: site.data.tweets %}
    {% assign sorted_entries = all_entries | sort: 'date' | reverse %}
    {% for entry in sorted_entries %}
      {% if entry.tweet_url %}
        <p style="margin-left: 5px;">
          𝕏 <a style="margin-left: 5px;" href="{{ entry.tweet_url }}" target="_blank">{{ entry.title | truncate: 45 }}</a>
        </p>
      {% else %}
        <p>🔥 <a href="{{ entry.url }}">{{ entry.title }}</a></p>
      {% endif %}
    {% endfor %}
</main>