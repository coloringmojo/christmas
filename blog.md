---
layout: default
title: "All Coloring Pages - Coloring Mojo"
---

# 📚 All Coloring Pages
*Complete Collection of Free & Premium Designs*

---

{% for post in site.posts %}
<div class="post-card">
    <h3>🎨 <a href="{{ post.url }}" style="text-decoration: none; color: inherit;">{{ post.title }}</a></h3>
    
    <div class="post-meta">
        📅 {{ post.date | date: "%B %d, %Y" }}{% if post.rating %} • ⭐ {{ post.rating }}{% endif %}
    </div>
    
    {{ post.excerpt | strip_html | truncate: 200 }}
    
    <div style="margin-top: 1rem;">
        <a href="{{ post.url }}" class="btn">View & Download →</a>
    </div>
</div>

{% unless forloop.last %}<hr>{% endunless %}
{% endfor %}

<div style="text-align: center; margin-top: 3rem;">
    <a href="/" class="btn btn-large">← Back to Home</a>
</div>
