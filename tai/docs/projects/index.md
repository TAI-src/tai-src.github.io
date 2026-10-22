# Projects

## Project Index

{% for p in glob("projects/*.md", hide=["project_template.md", "index.md"], page_path=page.file.src_path) %}

- [{{ p.title }}]({{ p.url }}) ({{ p.authors }})
{% endfor %}
