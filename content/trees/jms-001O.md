---
title: closure of positivity under directed suprema
taxon: lemma
tags: 
- uf
author:
- jonmsterling
date: 2023-02-14T09:42:42Z
macros:
- include: jms-001M
---

Let {#A#} be a [pointed](jms-001S) dcpo; the [positivity predicate](jms-001M) {#\Mor{\IsPos}{\Gamma A}{\Omega}#} is closed under directed suprema.

{{%proof%}}
Let {#J\subseteq A#} be a directed subset such that every {#u\in J#} is positive; we must show that {#\bigsqcup{J}#} is positive. Fixing a subdirected subset {#I\subseteq A#} such that {#\bigsqcup{J}\sqsubseteq \bigsqcup I#}, we must check that {#I#} is inhabited. The inequality {#\bigsqcup{J}\sqsubseteq \bigsqcup I#} holds if and only if {#u\sqsubseteq \bigsqcup{I}#} for all {#u\in u#}; as {#J#} is directed, we therefore have some positive {#u\in A#} such that {#u\sqsubseteq \bigsqcup{I}#} from which it follows that {#I#} is inhabited.
{{%/proof%}}
