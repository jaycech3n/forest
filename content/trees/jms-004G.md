---
title: the initial reflection algebra
taxon: theorem
tags: 
- uf
author:
- jonmsterling
date: 2023-03-22T08:02:30+01:00
macros:
- include: jms-0036
---

Let {#\UU\in\VV#} be an impredicative pair of universes with {#A:\VV#}. There we may construct a  [reflection algebra](jms-003O) {#A\Sub{\UU} :\Comma{A}{\UU}#} such that for any other [reflection algebra](jms-003O) {#X:\Comma{A}{\UU}#}, the space of [homomorphisms](jms-003O) {#A\Sub{\UU}\multimap X#} is contractible.

{{%proof%}}
Our [splitting of the generic element of the generic cone](jms-0044) {#\Mor{p}{\Delta I}{\Idn{\Comma{A}{\UU}}}#} over the identity functor on reflection algebras [yields a new (incoherent) cone](jms-003E) {#\Mor{q}{\Delta J}{\Idn{\Comma{A}{\UU}}}#} whose generic element {#q\Sub{J}:J\multimap J#} may be identified with the identity homomorphism. It [follows](jms-003B) that each  space of homomorphisms {#J\to X#} is contractible. Therefore, we define {#A\Sub{\UU}#} to be the apex {#J#}.
{{%/proof%}}
