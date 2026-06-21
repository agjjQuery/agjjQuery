---
layout:    default
title:     Menu • agjjQuery
permalink: /menu/
---

# Menu

<ul>
    {% assign site_title_with_semicolon = site.title | append: "&#58; " %}
    {% assign pages_sorted = site.pages | sort: "nav" %}
    {% for page in pages_sorted %}
        {% if page.nav %}
            <li>
                <a href="{{ page.url | prepend: site.baseurl }}" title="{{ page.title }}">
                    {{ page.title | replace: site_title_with_semicolon, "" }}
                </a>
            </li>
        {% endif %}
    {% endfor %}
    <li>
        <a href="https://twitter.com/agjjQuery" title="Twitter">Twitter</a>
    </li>
    <li>
        <a href="https://x.com/agjjQuery" title="𝕏">𝕏</a>
    </li>
    <li>
        <a href="https://patreon.com/agjopensource" title="Patreon">Patreon</a>
    </li>
</ul>
