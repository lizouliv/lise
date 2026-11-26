---
{"dg-publish":true,"permalink":"/references/dg-publish/","ctime":"2026-10-11T23:57:16.918+02:00","mtime":"2026-11-26T18:28:14.832+01:00","dg-note-properties":{"date created":"2026-10-11, 23 57","date modified":"2026-11-26, 18 28","sector":null,"semester":null,"class":null,"form":null,"part":null,"tags":[]}}
---


# dg-publish


```base
views:
  - type: table
    name: View
    filters:
      and:
        - file.hasProperty("dg-publish")
    order:
      - date created
      - file.name
      - dg-publish
      - file.path
    sort:
      - property: formula.Untitled
        direction: DESC
    columnSize:
      note.date created: 148
      file.name: 371
      note.dg-publish: 47

```
