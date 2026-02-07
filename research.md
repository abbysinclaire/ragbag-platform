---
layout: default
title: Research Archive
---

<h1>Research Archive</h1>
<p>All research inputs organized by date. Filter by tags to find specific topics.</p>

<div class="filter-section">
    <h3>All Tags</h3>
    <div class="all-tags">
    {% assign all_tags = site.research | map: 'tags' | join: ',' | split: ',' | uniq | sort %}
    {% for tag in all_tags %}
        {% if tag != "" %}
        <span class="tag">{{ tag }}</span>
        {% endif %}
    {% endfor %}
    </div>
</div>

<div class="research-archive">
{% assign sorted_research = site.research | sort: 'date' | reverse %}
{% for entry in sorted_research %}
    <article class="research-preview">
        <h2><a href="{{ entry.url | relative_url }}">{{ entry.title }}</a></h2>
        <div class="meta">
            <span class="date">{{ entry.date | date: "%B %d, %Y" }}</span>
            {% if entry.author %}
            <span class="author">by {{ entry.author }}</span>
            {% endif %}
        </div>
        {% if entry.excerpt %}
        <p>{{ entry.excerpt }}</p>
        {% endif %}
        {% if entry.tags %}
        <div class="tags">
            {% for tag in entry.tags %}
                <span class="tag">{{ tag }}</span>
            {% endfor %}
        </div>
        {% endif %}
    </article>
{% endfor %}
</div>
