---
title: "linear and thunkable maps"
tags:
- uf
author:
- jonmsterling
date: 2022-12-26T00:12:26+01:00
macros:
- include: base-macros
taxon: definition
---

Let {#f:C \vdash D#} be a morphism in a [deductive system](jms-0048) {#\mathcal{D}#}.

1. We say that {#f#} is *linear* when for all {#g:B\vdash C#} and {#h:A\vdash B#}, we have {#h;\prn{g;f} = \prn{h;g};f#}.

2. We say that {#f#} is *thunkable* when for all {#g:D\vdash E#} and {#h : E\vdash F#}, we have {#f;\prn{g;h} = \prn{f;g};h#}.
