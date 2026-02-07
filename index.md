---
layout: default
title: Home
---

<div class="hero">
    <h1>Welcome to RAGBAG</h1>
    <p>An independent research collective exploring ideas from scratch</p>
</div>

<section class="overview">
    <h2>Recent Research</h2>
    <ul class="research-list">
    {% assign sorted_research = site.research | sort: 'date' | reverse %}
    {% for entry in sorted_research limit:5 %}
        <li>
            <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
            <span class="date">{{ entry.date | date: "%b %d, %Y" }}</span>
            {% if entry.tags %}
                <div class="tags-inline">
                {% for tag in entry.tags %}
                    <span class="tag">{{ tag }}</span>
                {% endfor %}
                </div>
            {% endif %}
        </li>
    {% endfor %}
    </ul>
    <p><a href="{{ '/research/' | relative_url }}">View all research →</a></p>
</section>

<section class="overview">
    <h2>Our Members</h2>
    <ul class="member-list">
    {% for member in site.members %}
        <li>
            <a href="{{ member.url | relative_url }}">{{ member.name }}</a>
            {% if member.bio %}
            <p>{{ member.bio }}</p>
            {% endif %}
        </li>
    {% endfor %}
    </ul>
</section>
