---
title: dependent identity system
taxon: definition
tags: 
- uf
author:
- jonmsterling
date: 2023-03-22T09:09:05+01:00
macros:
- include: jms-003G
---

Let {#\mathcal{I}#} be an [identity system](jms-004J) on an element {#a:A#} and let {#B#} be a family of types over {#A#}. A *dependent identity system* over {#\mathcal{I}#} on an element {#b:Ba#} in the family {#B#} consists of a family of types {#\mathcal{J}\prn{x,q}#} over {#Bx#} for each {#x:A,q:\mathcal{I}x#} such that {#\mathcal{J}\prn{a,\Refl\Sub{I}}#} is equipped with the structure of an identity system on {#b : Ba#}. In particular, we have:

1. a distinguished element {#\Refl\Sub{\mathcal{J}} : \mathcal{J}\prn{a,\Refl\Sub{\mathcal{I}}}b#};
2. for each family {#P#} over {#\mathcal{J}\prn{a,\Refl\Sub{I}}#}, a dependent function {#J\Sub{\mathcal{J}}P : \Prod{p:P\prn{b,\Refl\Sub{\mathcal{J}}}}\Prod{y:Ba}\Prod{q:\mathcal{J}\prn{a,\Refl\Sub{\mathcal{I}}}y}{P\prn{y,q}}#} and a dependent function {#\beta\Sub{\mathcal{J}}P:\Prod{p:P\prn{b,\Refl\Sub{\mathcal{J}}}} \TpIdn{P\prn{b,\Refl\Sub{\mathcal{J}}}}{J\Sub{\mathcal{J}}p\,b\,\Con{refl}\Sub{\mathcal{J}}}{p}#}.
