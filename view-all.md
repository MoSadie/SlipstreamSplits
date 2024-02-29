{% assign pluto_splits = site.static_files | where: "pluto": true | sort: "path" %}
{% assign charon_splits = site.static_files | where: "charon": true | sort: "path" %}
{% assign neptune_splits = site.static_files | where: "neptune": true | sort: "path" %}
{% assign triton_splits = site.static_files | where: "triton": true | sort: "path" %}

## Pluto

{% for file in pluto_splits %}
- [{{ file.basename }}]({{ file.path | replace: "%", "%25"}})
{% endfor %}

## Charon

{% for file in charon_splits %}
- [{{ file.basename }}]({{ file.path | replace: "%", "%25"}})
{% endfor %}

## Neptune

{% for file in neptune_splits %}
- [{{ file.basename }}]({{ file.path | replace: "%", "%25"}})
{% endfor %}

## Triton

{% for file in triton_splits %}
- [{{ file.basename }}]({{ file.path | replace: "%", "%25"}})
{% endfor %}

[Return Home](/)