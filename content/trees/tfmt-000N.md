---
title: SVG is not an authoring language
author:
- jonmsterling
date: 2023-01-07T14:30:35+01:00
---

SVG is an extremely powerful low-level language for vector images and diagrams with a variety of applications. Unfortunately, it is not reasonable to compose such diagrams directly in SVG as an author: in contrast to programmatic tools like PGF/TikZ, all positions in SVG are fixed, and there is no possibility to impose important abstractions (e.g. the concept of a line that is "glued" to a pair of nodes). On the other hand, there are many advantages to SVG, including the possibility to [intermix SVG with other formats such as MathML](tfmt-000M).

Because of the low level of abstraction, SVG images that appear in practice today are nearly always produced by a tool or compiler from an input that is defined at a much higher level of abstraction.
