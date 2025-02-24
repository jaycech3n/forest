---
title: positively generated pointed dcpos are free
tags:
- uf
taxon: lemma
author:
- tomdejong
- martinescardo
- jonmsterling
date: 2023-02-16T15:32:41Z
macros: 
- include: jms-0021
---

Let {#A#} be a [positively generated](jms-0023) [pointed](jms-001S) dcpo; then {#A#} is canonically *free* on its [subdcpo of positive elements](jms-001P) {#A^+#}. More specifically, the embedding-projection pair {#\prn{\Lift{\iota^+};\alpha_A}\dashv\Mor{\Purify_A}{A}{\Lift{A^+}}#} [given by](jms-0020) the [purification map](jms-0021) is an isomorphism of dcpos.

{{%proof%}}
First, we recall that the embedding-projection pair {#\prn{\Lift{\iota^+};\alpha_A}\dashv\Purify_A#} exists because {#A#} has an [open positivity predicate](jms-0022) by [virtue of](jms-0027) its [positive generation](jms-0023). Therefore, the statement of this lemma is well-formed.

Because {#\prn{\Lift{\iota^+};\alpha_A}\dashv\Purify_A#} is an embedding-projection pair, it remains only to check that {#\Purify_A;\Lift{\iota^+};\alpha_A#} is an *inflation*, i.e. for all {#a:A#} we must have {#a \sqsubseteq \alpha_A\prn{\Lift{\iota^+}\prn{\Purify_Aa}}#}. As the latter is equal to {#\bigsqcup_{p:\IsPos\,a}a#}, the inflation condition follows from our assumption that {#A#} is [positively generated](jms-0023).
{{%/proof%}}
