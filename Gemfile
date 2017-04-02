---
layout: default
---

{% for post in paginator.posts %}
<article class="post" role="article" itemscope itemtype="http://schema.org/BlogPosting">
    <header class="post-header">
        <ul class="clear">
            <li><time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%-d %b, %Y" }}</time></li>
            {% if site.show_categories == 1 and post.category %}
                <li class="cats">
                    {% for category in post.category %}
                        <a href="{{site.baseurl}}/{{site.category_dir}}/{{category}}/">{{ category }}</a>
                    {% endfor %}
                </li>
            {% endif %}
        </ul>
        <h2 itemprop="name headline"><a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}">{{ post.title }}</a></h2>
    </header>

    <div class="post-content">
        {{ post.excerpt }}

        {% if post.excerpt != post.content %}
            <p><a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}" role="button">Read More</a></p>
        {% endif %}
    </div>

    <footer class="post-footer">
        {% if site.show_mood == 1 and post.mood %}
        <div class="mood {{ post.mood }}" title="{{ post.mood | capitalize }}">Mood</div>
        {% endif %}
        <div class="share">Share
            <ul class="social-networks">
                <li class="share-facebook"><a href="https://www.facebook.com/sharer.php?s=100&p[title]={{post.title | strip_html }}&p[summary]={{post.excerpt | strip_html | truncate: 140 }}&p[url]={{ post.url | prepend: site.baseurl | prepend: site.url }}" class="s_facebook" target="_blank" onclick="window.open(this.href, '','width=700,height=300');return false;"><svg title="" width="16" height="16"><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="{{ site.baseurl | prepend: site.url }}/assets/svg/social-icons.svg#facebook-icon"></use></svg></a></a></li>
                <li class="share-twitter"><a href="http://twitter.com/share?url={{post.url | prepend: site.url | escape}}&text={{ post.excerpt | strip_html | truncate: 140 }}&hashtags={% for tag in post.tags %}{{ tag }},{% endfor %}" rel="noreferrer" target="_blank" onclick="window.open(this.href, '','width=700,height=300');return false;"><svg title="" width="16" height="16"><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="{{ site.baseurl | prepend: site.url }}/assets/svg/social-icons.svg#twitter-icon"></use></svg></a></li>
            </ul>
        </div>
        {% if site.show_tags == 1 and post.tags %}
        <div class="tags">
            <ul>
                {% for tag in post.tags %}
                <li><a href="{{ site.baseurl | prepend: site.url }}/tag/{{ tag }}">{{ tag }}</a></li>
                {% endfor %}
            </ul>
        </div>
        {% endif %}
    </footer>
</article>
{% endfor %}

{% if paginator.total_pages > 1 %}
<div class="pagination clear" role="navigation" aria-label="pagination">
    {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path }}" class="previous">&larr; Previous</a>
    {% endif %}

    <span class="page_number">Page {{ paginator.page }} of {{ paginator.total_pages }}</span>

    {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path }}" class="next">Next &rarr;</a>
    {% endif %}
</div>
{% endif %}