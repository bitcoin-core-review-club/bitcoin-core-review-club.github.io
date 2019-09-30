{% capture /dev/null %}
{% assign path = page.path | remove: ".html" %}
{% if path == "meetings" %}
  {% assign _index_links = _index_links | append: "<strong>by date</strong>" %}
{% else %}
  {% assign _index_links = _index_links | append: "<a href='/meetings'>by date</a>" %}
{% endif %}
{% if path == "meetings-components" %}
  {% assign _index_links = _index_links | append: " | <strong>by component</strong>" %}
{% else %}
  {% assign _index_links = _index_links | append: " | <a href='/meetings-components'>by component</a>" %}
{% endif %}
{% if path == "meetings-hosts" %}
  {% assign _index_links = _index_links | append: " | <strong>by host</strong>" %}
{% else %}
  {% assign _index_links = _index_links | append: " | <a href='/meetings-hosts'>by host</a>" %}
{% endif %}
{% endcapture %}
| {{_index_links}} |
