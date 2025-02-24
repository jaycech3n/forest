---
title: MathML is not an authoring language
author:
- jonmsterling
date: 2023-01-07T14:42:26+01:00
lastmod: 2023-01-08
---

Despite some preliminary support for structured representation of high-level mathematical idioms via [Content MathML](https://www.w3.org/TR/MathML/chapter4.html), MathML is not intended to be an authoring language: it is a target language for other tools. Moreover, the content dictionaries (collections of basic elements) of Content MathML are chosen to pertain to the needs of grade-school and secondary-school mathematics and not at all to the needs of professional mathematics:

> The base set of content elements is chosen to be adequate for simple coding of most of the formulas used from kindergarten to the end of high school in the United States, and probably beyond through the first two years of college, that is up to A-Level or Baccalaureate level in Europe.

Nonetheless, it seems that the goal was for the content dictionaries of Content MathML to be extended by the individual "communities of practice" to meet their specific needs:

>  Hence, it is not in general possible for a user agent to automatically determine the proper interpretation for `definitionURL` values without further information about the context and community of practice in which the MathML instance occurs.

> However, in contexts where highly precise semantics are required (e.g. communication between computer algebra systems, within formal systems such as theorem provers, etc.) it is the responsibility of the relevant community of practice to verify, extend or replace definitions provided by OpenMath CDs as appropriate.

It seems that there is a possibility [to use XSLT](https://www.data2type.de/xml-xslt-xslfo/math-ml/styles-transformations/xslt-with-mathml/create-macros) to define your own semantic notational macros, and this certainly bears further investigation. Due to the mutually reinforcing combination of historically poor vendor support and near-absolute isolation from actual communities of practice, i.e. working mathematicians, sophisticated direct use of MathML has never caught on. On the other hand, there is a great deal of MathML on the web today in the form of [MathJax](https://www.mathjax.org/) and [{#\KaTeX#}](https://www.katex.org/) output --- tools which are not only currently necessary for obtaining consistent (and professional-quality) rendering of mathematics across browsers, but also are necessary for authoring due to their more succinct markup and easy support for macros.

It seems that the future of MathML is brighter than it was in the past, as we are finally seeing a vital project to improve vendor support led by [Igalia](https://mathml.igalia.com). Currently, even browsers that support the MathML standard do so with completely inadequate and unprofessional rendering quality, which means that tools like MathJax and {#\KaTeX#} may remain necessary for some time even after vendors finally support MathML. But we hope that with improved vendor support comes new and productive experiments with using semantic tools like XSLT to handle macros, etc. Unfortunately, given the [tight coupling between the authoring of mathematical expressions and of mathematical diagrams](tfmt-000P), this transformation will not take place unless high-level hypertext-compatible tools for drawing diagrams are simultaneously developed.
