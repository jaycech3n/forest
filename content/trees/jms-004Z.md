---
title: uniqueness of downshifts
author:
- jonmsterling
date: 2023-04-15T16:28:58+02:00
taxon: lemma
macros:
- include: jms-004M
---

Let {#N\in\mathcal{D}#} be a [negative](jms-004B) object in a [positively univalent deductive system](jms-004Q); then the type of [downshift structures](jms-004P) on {#N#} is a proposition. In this case, we may refer to the property of {#N#} *having a downshift*.

{{%proof%}}
Let {#w_0:N\vdash P_0#} and {#w_1:N\vdash P_1#} be two [downshift structures](jms-004P) on {#N#}, whose inverse unwrapping maps are written {#u_0,u_1#} respectively. We wish to identity {#\prn{P_0,w_0}#} with {#\prn{P_1,w_1}#}.

All four maps {#w_0,w_1,u_0,u_1#} are thunkable: the wrapping maps are thunkable by definition, and the unwrapping maps are thunkable because they are valued in a negative object. Thus we have a thunkably invertible thunkable map {#u_1;w_0 : P_1\vdash P_0#}; because {#\mathcal{D}#} is assumed [positively univalent](jms-004Q), we may identify the pairs {#\prn{P_0,\Idn{P_0}:P_0\vdash P_0}#} and {#\prn{P_1, \prn{u_1;w_0:P_1\vdash P_0}}#}. Taking inverses and precomposing with {#w_0#} on both sides, we have {#\prn{P_0,w_0} = \prn{P_1,w_1}#} using the fact that {#w_0#} is thunkable and inverse to {#u_0#}.
{{%/proof%}}
