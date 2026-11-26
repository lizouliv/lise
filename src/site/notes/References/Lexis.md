---
{"dg-publish":true,"permalink":"/references/lexis/","ctime":"2026-11-18T18:49:39.436+01:00","mtime":"2026-11-26T18:27:59.695+01:00","dg-note-properties":{"date created":"2026-11-18, 18 50","date modified":"2026-11-18, 18 50","sector":"[[References]]","semester":null,"class":null,"form":"[[References/Lexis]]","part":null,"tags":[]}}
---


# Lexis 360 Intelligence — Documentation externe

> [!info] Documentation séparée des cours
> Cet espace regroupe exclusivement les fiches de documentation **Lexis 360 Intelligence** (*Fiches pédagogiques*, *Fiches pratiques*, *Synthèses JurisClasseur*) dans `Lexis 360/` et leurs PDF sources dans `Attachments/Lexis 360/`, sans mélange avec tes notes de `[[CM]]`, `[[TD]]` ou `[[Notion]]` personnelles.


```base
views:
  - type: table
    name: Documentation Lexis 360
    filters:
      and:
        - sector == link("Lexis")
        - '!file.inFolder("References")'
    order:
      - file.name
      - class
      - semester
    sort:
      - property: class
        direction: ASC
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 480

```

