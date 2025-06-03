---
layout: page
title: "Home"
class: home
---

# Hi, I'm Pengzhu Lin

<div class="columns" markdown="1">

<div class="intro" markdown="1">
Dr. Pengzhu Lin is a post-doctoral fellow at [the Hong Kong University of Science and Technology](https://hkust.edu.hk/) currently.  He received his Ph.D. in Mechanical Engineering from [the Hong Kong University of Science and Technology](https://hkust.edu.hk/) in 2024, and his M.S. and B.S. from [Huazhong University of Science and Technology](https://www.hust.edu.cn/) in 2020 and 2017. His research focuses on heat and mass transfer, energy storage, energy conversion, such as fuel cells and batteries, combining with artificial intelligence. He has published papers on top journals including ACS Energy Letters, Applied Energy, International Journal of Heat and Mass transfer, etc.

Find me on [GitHub](https://github.com/pengzhulin), [LinkedIn](https://www.linkedin.com/in/dominik-moritz-409b8124/), or [Twitter](https://twitter.com/domoritz).
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/pengzhu_photo.png' type='image/png' />
  <img
    src='/images/pengzhu_photo.png'
    alt='Pengzhu Lin'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* Room 4001, CYT Building
</div>

</div>

I have worked with the [Prof. T.S. Zhao](https://ai.google/research/), [Google Research](https://ai.google/research/), [Microsoft Research](https://www.microsoft.com/en-us/research/group/vibe/), and others. Details are in my [CV]({{ "/cv/" | relative_url }}).

## Featured <a href="{{ "/projects/" | relative_url }}">Projects</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Featured <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>
