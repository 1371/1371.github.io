---
layout: page
title:  "Портфолио"
permalink: "/portfolio/"
---

<figure>
    <img src="https://d13yacurqjgara.cloudfront.net/users/239125/screenshots/2591055/littleprincedribbble.jpg" />
    <figcaption>Created by <a href="https://dribbble.com/Pmafra" target="_blank_">Patricia Mafra</a></figcaption>
</figure>

In addition to writing posts, another thing you may want to do with your Jekyll site is create static pages. By taking advantage of the way Jekyll copies files and directories, this is easy to do. [More Information](https://jekyllrb.com/docs/pages/){:target="_blank"}

{% if paginator.total_pages > 1 %}
<div class="pagination clear" role="navigation" aria-label="pagination">
    {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path }}" class="previous">&larr; Назад</a>
    {% endif %}

    <span class="page_number">Страница {{ paginator.page }} из {{ paginator.total_pages }}</span>

    {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path }}" class="next">Вперед &rarr;</a>
    {% endif %}
</div>
{% endif %}