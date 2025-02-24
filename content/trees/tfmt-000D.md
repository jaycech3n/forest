---
title: implicit vs. explicit hierarchy in document markup languages
author:
- jonmsterling
date: 2022-12-29T13:59:02+01:00
---

Many document markup languages, including {#\LaTeX#} and HTML, use sectioning commands that evince an *implicit* hierarchical structure: for instance, consider the following HTML code:

```html
<h1>Foo</h1>
<h2>Bar</h2>
<h3>Baz</h3>
<h3>Qux</h4>
<h1>Boo</h1>
```

The above corresponds to the tree `[Foo > [Bar > [Baz, Qux]], Boo]`. On the other hand, it is also possible to consider a model in which the hierarchy is made explicit through the syntactical tree structure of the markup language. This style is also supported (but not forced) in HTML:

```html
<section>
  <h1>Foo</h1>
  <section>
    <h2>Bar</h2>
    <section>
      <h3>Baz</h3>
    </section>
    <section>
      <h3>Qux</h3>
    </section>
  </section>
</section>

<section>
  <h1>Boo</h1>
</section>
```
