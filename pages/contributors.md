---
sidebar: home_sidebar
title: LineageOS contributors
permalink: contributors.html
versions: [14.1, 13.0]
---

{% assign devices = "" | split: " " %}
{% for device in site.data.devices %}
{% assign devices = devices | push: device[1] %}
{% endfor %}
{% assign sorted = devices | sort: 'name' | sort: 'vendor' %}

## Maintainers

### Head developers

Head developers have extensive knowledge of the OS, and are project leads. These people have responsibility over the direction of
the project and are committed to improving it.

| Name | Nickname |
|------|----------|
| Chirayu Desai | cdesai |
| Dan Pasanen | invisiblek |
| Daniel Hillenbrand | codeworkx |
| Danny Baumann | maniac103 |
| Diogo Ferreira | defer |
| Ed Carrigan | senyor |
| Ethan Chen | intervigil |
| Marcos Marado | marado |
| Michael Bestas | mikeioannina |
| Tom Marshall | tdm |

### Trusted reviewers

Trusted reviewers are known to provide consistent constructive feedback in line with project rules and guidelines. As a result, 
their feedback is held as backed by project leads and recognized as a distinct group from general public reviewers.

| Name | Nickname |
|------|----------|
| Arne Coucheron | arco |
| Björn Lundén | blunden |
| Brandon McAnsh | bmc08gt |
| Christopher R Palmer | crpalmer |
| Kevin Haggerty | haggertk |
| Michael W. | BadDaemon |
| Scott Warner | Tortel |
| Shane Passmore | h8rift |
| Simon Shields | forkbomb |

### Committers

Committers are responsible for testing commits and merging them in high flowrate situations. These developers have merge rights across the board.

| Name | Nickname |
|------|----------|
| Brinly Taylor | brinlyau |
| Christopher N. Hesse | raymanfx |
| Clark Scheff | D34D |
| Joey Rizzoli | joeyrizzoli |
| Luca Stefani | luca020400 |
| Luk1337 | Luk1337 |
| Rashed Abdel-Tawab | rashed |
| Zhao Wei Liew | zwliew |

### Developer relations managers

Developer relations managers are responsible for running the day-to-day infrastructure and for keeping the health of the project.
Although everyone has a responsibility to help new people join the community and protect the project’s health, these people maintain the contribution
pathways that connect to potential contributors to teams that have contribution opportunities and grant new device maintainers access to devices.

| Name | Nickname |
|------|----------|
| Abhisek Devkota | ciwrl |
| Tom Powell | zifnab |

### Device maintainers

{% for version in page.versions %}

#### LineageOS {{ version }}

<table>
<thead>
<tr><th>Device</th><th>Maintainer(s)</th></tr>
</thead>
<tbody>
{% for device in sorted %}
{% assign length = device.channels | size %}
{% if device.current_branch != version or length == 0 %}
{% continue %}
{% endif %}
<tr><td><b><a href="{{ "/devices/" | append: device.codename | relative_url }}">{{ device.vendor }} {{ device.name }} ({{ device.codename }})</a></b></td><td>{{ device.maintainers | join: ', ' }}</td></tr>
{% endfor %}
</tbody>
</table>
{% endfor %}

## Translations

### Translations managers

<table>
<thead>
<tr><th>Name</th><th>Nickname</th></tr>
</thead>
<tbody>
{% for el in site.data.translators.managers %}
<tr><td>{{ el.name }}</td><td>{{ el.nick }}</td></tr>
{% endfor %}
</tbody>
</table>

### Translations proofreaders

{% for lang in site.data.translators.languages %}
* __{{ lang.name }}__: {{ lang.proofreaders | join: ', ' }}
{% endfor %}

## Other projects

### Mirror manifest

The mirror manifest can be found [here](https://www.github.com/LineageOS/mirror).

| Name           | Nickname  |
|----------------|-----------|
| Tim Schumacher | TimSchumi |

### Website

These persons are responsible for the content of [our website](https://www.lineageos.org/):

| Name            | Nickname   |
|-----------------|------------|
| Abhisek Devkota | ciwrl      |
| Dan Pasanen     | invisiblek |
| Harry Youd      | harryyoud  |
| Tom Powell      | zifnab     |

### Wiki

If you want to contribute to the wiki yourself, you can find instructions on how to do so [here]({{ "contributing.html" | relative_url }}).
The following people are responsible for the verification of the contents and the general maintenance of the wiki:

| Name           | Nickname   |
|----------------|------------|
| Bruno Martins  | bgcngm     |
| Evan Widger    | psychoi3oy |
| Michael W      | baddaemon  |
| Simon Shields  | fourkbomb  |
| razorloves     | razorloves |
