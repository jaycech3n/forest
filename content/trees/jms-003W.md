---
title: semicoherence structure
taxon: definition
tags:
- uf
author:
- jonmsterling
date: 2023-03-15T15:48:25+01:00
macros:
- include: jms-0036
---

Let {#\UU\in\VV#} be an impredicative universe pair with {#A:\VV#} such that {#\IncohNatStr#} is the [displayed reflection algebra](jms-003R) of [incoherent naturality structures](jms-003V) over the [product](jms-003Q) {#\Prod{X:\Comma{A}{\UU}}X#} of all [reflection algebras](jms-003O). We define a further [displayed reflection algebra](jms-003T) {#\SemicohStr#} over {#\IncohNatStr#} of "semicoherence structures" associating to each [incoherent naturality structure](jms-003V) one dimension of coherence data for binary compositions of [homomorphisms](jms-003O).

In particular, we define {#\SemicohStr#} over {#\widetilde{\IncohNatStr}#} as follows, employing our notion of [homotopy between homomorphisms](jms-003X):
{##
  \begin{array}{l}
    \SemicohStr[u] :\equiv\\
    \begin{array}{l}
    \Prod{\brc{X,Y,Z:\Comma{A}{\UU}}}
    \Prod{f : X\multimap Y}
    \Prod{g : Y\multimap Z}
    \Prod{h : X \multimap Z}
    \Prod{\phi : \TpHtpy{X\multimap Z}{f;g}{h}}\\
    \Con{ap}\Sub{g} \prn{\vartheta\Sub{u} f} \bullet \vartheta\Sub{u} g 
    = \phi\prn{\epsilon\Sub{u} X} \bullet \vartheta\Sub{u} h
    \end{array}
  \end{array}
##}

To define the displayed algebra structure {#\bar\eta\Sub{\SemicohStr}#}, we will use the contractibility of singletons several times. In particular, given {#\prn{Y,f}#} where {#Y:\Comma{A}{\UU}#} and {#f:X\multimap Y#}, the algebra component {#\eta\Sub{Y}#} is completely determined by the homotopy {#\eta\Sub{f} :\TpHtpy{A\to Y}{\eta\Sub{Y}}{f \circ \eta\Sub{X}}#}; likewise, by our [characterization of paths between homomorphisms](jms-003Y), the pair {#\prn{h,\phi}#} is uniquely determined. Therefore, we may define {#\bar\eta\Sub{\SemicohStr}#} to be the unique function satisfying the following equation:

{##
\bar\eta\Sub{\SemicohStr}\,a\,\prn{f,\lambda\_.\Refl}\,\prn{g,\lambda\_.\Refl}\,\prn{\prn{f;g},\lambda\_.\Refl}, \prn{\lambda\_.\Refl,\lambda\_.\Refl} := \Refl
##}

Given an element {#u:\widetilde{\SemicohStr}#}, we shall write {#\epsilon\Sub{u},\vartheta\Sub{u}#} for the components of its underlying [incoherent naturality structure](jms-003V) {#\pi\Sub{\SemicohStr}u#} and {#\varsigma\Sub{u} : \SemicohStr[\pi\Sub{\SemicohStr}u]#} for the semicoherence structure itself.

This definition is similar to that of [Awodey, Frey, and Speight](awodey-frey-speight-2018), except that we do not impose any coherence law for identities.
