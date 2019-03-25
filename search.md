---
layout: default

---
<h1>Search Results</h1>
<ul id="search-results"></ul>

<script>
  window.store = {
    {% for post in site.posts %}
      "{{ post.url | slugify }}": {
        "title": "{{ post.title | xml_escape }}",
        "category" : "{{post.categories | join: ', '}}",
        "tags"     : "{{ post.tags | join: ', ' }}",
        "description" : "{{post.description | strip_html | strip_newlines | escape }}",
        "url": "{{ post.url | xml_escape }}"
      }
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  };
</script>
<script src="https://unpkg.com/lunr/lunr.js"></script>
<script src="/inc/search.js"></script>