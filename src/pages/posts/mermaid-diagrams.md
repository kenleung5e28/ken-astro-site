---
title: "Mermaid Diagrams"
date: 2020-11-08T21:32:20+08:00
draft: false
mermaid: true
---

Diagram 1

{{<mermaid>}}
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
{{</mermaid>}}

Diagram 2

{{<mermaid>}}
graph TD;
  A-->B;
  A-->C;
  B-->C;
  B-->D;
  C-->D;
  D-->B;
{{</mermaid>}}