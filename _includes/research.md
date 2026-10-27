<h2 id="research" style="margin: 2px 0px -15px;">Research</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.research.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.video %}
    <video class="teaser img-fluid z-depth-1" width="270" height="123" autoplay muted loop playsinline preload="metadata" poster="{{ link.image }}" aria-label="{{ link.title }} preview">
      <source src="{{ link.video }}" type="video/mp4">
    </video>
    {% elsif link.image %}
    <img src="{{ link.image }}" alt="{{ link.title }}" class="teaser img-fluid z-depth-1">
    {% endif %}
    {% if link.badge %}{% if link.video or link.image %}
    <abbr class="badge">{{ link.badge }}</abbr>
    {% endif %}{% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      {% assign title_url = link.pdf | default: link.page | default: link.code %}
      <div class="title">{% if title_url %}<a href="{{ title_url }}">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
      {% if link.authors %}
      <div class="author">{{ link.authors }}</div>
      {% endif %}
      {% if link.meta %}
      <div class="entry-meta">{{ link.meta }}</div>
      {% endif %}
      <div class="periodical"><em>{% if link.status %}{{ link.status }}{% if link.date %} · {% endif %}{% endif %}{{ link.date }}</em>
      </div>
      {% if link.description %}
      <div class="description">{{ link.description }}</div>
      {% endif %}
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.notes %}
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
