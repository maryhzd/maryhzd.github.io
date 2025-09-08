<h2 id="conferences" class="mb-3">Conferences</h2>

<div class="conferences">
  <ol class="bibliography list-unstyled">
    {% for link in site.data.conferences.main %}
    <li class="mb-4">
      <div class="row pub-row g-3 align-items-start">
        <div class="col-sm-3 abbr">
          {% if link.image %}
            <img src="{{ link.image | relative_url }}" class="teaser img-fluid z-depth-1" alt="Teaser for {{ link.title }}" style="width:100%; height:auto;">
          {% endif %}
          {% if link.conference_short %}
            <span class="badge bg-secondary mt-2">{{ link.conference_short }}</span>
          {% endif %}
        </div>
        <div class="col-sm-9">
          <div class="title">
            {% if link.pdf %}
              <a href="{{ link.pdf | relative_url }}" target="_blank" rel="noopener">{{ link.title }}</a>
            {% elsif link.page %}
              <a href="{{ link.page | relative_url }}" target="_blank" rel="noopener">{{ link.title }}</a>
            {% else %}
              {{ link.title }}
            {% endif %}
          </div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>
          <div class="links mt-1">
            {% if link.pdf %}
              <a href="{{ link.pdf | relative_url }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">PDF</a>
            {% endif %}
            {% if link.code %}
              <a href="{{ link.code }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Code</a>
            {% endif %}
            {% if link.page %}
              <a href="{{ link.page | relative_url }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Project Page</a>
            {% endif %}
            {% if link.bibtex %}
              <a href="{{ link.bibtex | relative_url }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">BibTeX</a>
            {% endif %}
            {% if link.notes %}
              <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
            {% endif %}
            {% if link.others %}
              {{ link.others }}
            {% endif %}
          </div>
        </div>
      </div>
    </li>
    {% endfor %}
  </ol>
</div>
