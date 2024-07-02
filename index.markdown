---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Index

## [Maths PSI](/MathsPSI/index.markdown)

## [Physique MPSI](/PhysiqueMPSI/index.markdown)

<video autoplay="true" loop="loop" src="https://raw.githubusercontent.com/vcncolin/lefrenchmathproject/main/assets/manim/GaussianFunction.mp4" width="640" height="480" controls></video>

<ul>
{% for page in site.pages %}
    {% if page.categories =="index" %}
        <li><a href="{{ page.url }}">{{ page.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>