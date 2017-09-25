{%
if include.framed and include.framed == "yes" %}{%
  assign class = "border" %}{%
else %}{%
  assign class = "" %}{%
endif %}
{%
if include.position and include.position == "right" %}{%
  assign pos = "pull-right gap-left" %}{%
elsif include.position and include.position == "left" %}{%
  assign pos = "pull-left gap-right" %}{%
else %}{%
  assign pos = "image-block" %}{%
endif %}
<div class="{{ pos }}">
  <div class = "image-container {{ class }}" style="width: {{ include.width | plus: 20 }}px;">
    <a href="{{ site.baseurl }}{{ site.imageurl }}/{{ include.file }}"
      data-lightbox="blog" data-title="{{ include.caption }}">
      <img src="{{ site.baseurl }}{{ site.imageurl }}/{{ include.file }}"
        title="{{ include.caption }}" {%
          if include.width %} width="{{ include.width }}px" {% endif %}{%
          if include.height %} height="{{ include.height }}px" {% endif %}>
    </a>
    <div class="image-caption">{{ include.caption }}</div>
  </div>
</div>
