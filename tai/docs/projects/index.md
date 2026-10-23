# Projects

{% set colors = {
    "lit": "#174A8B",
    "exp": "#168CBB",
    "app": "#5267A9",
    "rec": "#168C83",
    "bench": "#B56518"
} %}

This is a list of current and past projects related to the TAI initiative. Each project is categorized based on its research theme, which is color-coded for easy identification. For background on the themes, please refer to the [About page](../about.md#research-themes).

- Example Collection and Analysis:
    - <span style="color: {{ colors.lit }};">Existing Literature</span>
    - <span style="color: {{ colors.exp }};">Expert Experience</span>
    - <span style="color: {{ colors.app }};">Application Example</span>
- <span style="color: {{ colors.rec }};">Recurring Problems</span>
- <span style="color: {{ colors.bench }};">Benchmarking Suites and Methodology</span>

## Project Index

{% for p in glob("projects/*.md", hide=["project_template.md", "index.md"], page_path=page.file.src_path) %}

- <a href="{{ p.url }}" style="color: {{ colors.get(p.category, '#000000') }};">{{ p.title }}</a> ({{ p.authors }})

{% endfor %}
