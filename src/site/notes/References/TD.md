---
{"dg-publish":true,"permalink":"/references/td/","ctime":"2026-10-05T11:38:24.338+02:00","mtime":"2026-11-26T18:27:59.763+01:00","dg-note-properties":{"date created":"2026-10-05, 11 38","date modified":"2026-10-05, 11 41","sector":"[[References]]","semester":null,"class":null,"form":null,"part":null,"tags":[]}}
---


# TD

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - semester == link("S3")
        - "!form.isEmpty()"
        - sector != link("Lexis")
        - '!file.inFolder("Lexis 360")'
    order:
      - file.name
      - semester
      - class
      - form
    sort:
      - property: form
        direction: ASC
      - property: semester
        direction: ASC

```
