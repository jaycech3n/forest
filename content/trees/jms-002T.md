---
title: characterization of positivity in terms of partial elements
taxon: theorem
tags: 
- uf
author:
- jonmsterling
date: 2023-02-21T13:29:42-05:00
macros:
- include: jms-001M
---

Let {#A#} be a [pointed](jms-001S) dcpo. Then an element {#a:A#} is [positive](jms-001M) if and only if for any partial element {#u: LA#} such that {#a\sqsubseteq\bigsqcup_{p:u{\downarrow}}u[p]#}, we have {#u{\downarrow}=\top#}.

{{%proof%}}
Therefore, we first suppose that any {#u: LA#} is defined supposing {#a\sqsubseteq\bigsqcup_{p:u{\downarrow}}u[p]#} to check that {#a#} is [positive](jms-001M). Fixing a semidirected subset {#I\subseteq A#} such that {#a\sqsubseteq \bigsqcup{I}#}, we must show that {#I#} is inhabited.
We consider the partial element {#u=\prn{\exists i\in I. \top, \lambda\_.\bigsqcup{I}}:LA#}, and observe that {#\bigsqcup{I}=\bigsqcup_{i\in I} \bigsqcup{I}=\bigsqcup_{p:u{\downarrow}}u[p]#}, and so we have {#a\sqsubseteq \bigsqcup_{p:u{\downarrow}}u[p]#} and thus it follows that {#u{\downarrow}=\top#} and so {#I#} is inhabited.

Conversely, if {#a#} is [positive](jms-001M), it follows that any partial element {#u#} is defined when {#a\sqsubseteq\bigsqcup_{p:u{\downarrow}}u[p]#}, because the subset {#\brc{y\mid y=a\land u{\downarrow}}#} is semidirected.
{{%/proof%}}
