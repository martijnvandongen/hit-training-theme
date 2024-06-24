---
title: "Slides Markup"
---

[Open Slide Deck 1](deck1)

### Backgrounds

Check out all options for [backgrounds on the revealjs website](https://revealjs.com/backgrounds/).

Video: 
```text
<!-- .slide: data-background-video="https://static.schubergphilis.com/media/videos/Schuberg_header_LR-v2.mp4" data-background-video-loop data-background-video-muted data-background-color="black" -->
```

Gradient:

```text
<!-- .slide: data-background-gradient="linear-gradient(to bottom, #fff, #17b2c3)" -->
```

Image:

```text
<!-- .slide: data-background-color="black" data-background-image="/01-jump-start/20-part-1/10-amazon-aws/img/cpu-microscope.jpg" -->
```

### Element Attributes

```text
- Item 1 <!-- .element: class="fragment" data-fragment-index="2" -->
- Item 2 <!-- .element: class="fragment" data-fragment-index="1" -->
```

### Code

Choose `text` or other languages such as `python`, `json` or `yaml` to use code highlighting.

Choose `[]` and row numbers to higlight specific lines during the presentation. First it will show slides `1` and `4-7`, when you click it will highlight only row `8`.

{{< code >}}
```text [1,4-7|8]
Here's some content
```
{{< /code >}}