---
layout: default
title: Members
---

<h1>RAGBAG Members</h1>
<p>Each member documents their seasonal exploration project here.</p>

<div class="members-grid">
{% for member in site.members %}
    <div class="member-card">
        <h2><a href="{{ member.url | relative_url }}">{{ member.name }}</a></h2>
        {% if member.bio %}
        <p>{{ member.bio }}</p>
        {% endif %}
        {% if member.tags %}
        <div class="tags">
            {% for tag in member.tags %}
                <span class="tag">{{ tag }}</span>
            {% endfor %}
        </div>
        {% endif %}
    </div>
{% endfor %}
</div>
