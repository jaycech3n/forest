---
title: positively generated elements are non-negatively generated
taxon: lemma
tags: 
- uf
author:
- jonmsterling
date: 2023-02-16T18:10:46Z
macros:
- include: jms-001M
---

Let {#a#} be a [positively generated element](jms-002F) of a [pointed](jms-001S) dcpo {#A#}. Then {#a#} is also [non-negatively generated](jms-002J).

{{%proof%}}
We must check that {#a\sqsubseteq \bigsqcup_{p:\lnot\prn{a = \bot}}a#}. By assumption, it suffices to check that {#\bigsqcup_{p:\IsPos\,a}a\sqsubseteq\bigsqcup_{p:\lnot\prn{a=\bot}}a#}, which follows because [the bottom element is not positive](jms-002H).
{{%/proof%}}
