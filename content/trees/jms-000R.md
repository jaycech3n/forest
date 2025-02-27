---
title: background on homotopy and cubical type theory
author:
- jonmsterling
date: 2023-01-19T13:17:16-05:00
---

For more than four decades, dependent type theory has been positioned as the "common language" that can finally [unify mathematics and computer programming](martin-loef-1982): while it has never been controversial that a computer program is a form of mathematical construction, the running hypothesis of the type theoretic community has been the converse to this claim, namely that mathematical constructions should be viewed as programs that can in principle be executed by a physical machine --- roughly, **sets** = **types** and **elements** = **programs**. Thus the struggle to realize this type theoretic hypothesis has been a two-way process, punctuated by moments at which the mathematical meaning of a programming construct is elucidated, or at which the computational content of a mathematical construct is uncovered.

In the current millennium, a new identification has been taking shape in which **types** = **<span class="nowrap">{#\infty#}-groupoids</span>** (homotopy types), which are an infinite-dimensional generalization of sets; the origins of this new perspective on type theory lie with [Hofmann and Streicher's 1998 groupoid interpretation of type theory](hofmann-streicher-1998), combined with the revolutionary contributions of [Voevodsky](voevodsky-2006) and [Awodey and Warren](awodey-warren-2009) respectively. The main feature of the new language, dubbed [**homotopy type theory**](hottbook) or **HoTT**, is that isomorphisms between types are equipped with a new induction rule called univalence stating that all type theoretic constructs respect isomorphisms: to a first approximation, if {#A \cong B#} then {#P(A) \cong P(B)#} for any {#P#}. The univalence principle is motivated by the phenomenon of homotopy invariance that pervades the large-scale structure of modern-day mathematics, from algebraic topology to algebraic geometry to mathematical physics; as a programming construct, univalence suggests [new approaches](acmz-2021) to both generic and modular programming.

Thus one of the main projects for the first decade of homotopy type theory was to substantiate the relationship between HoTT and mathematics on the one hand, and between HoTT and computer programming on the other hand. The question of whether homotopy type theoretic language can be interpreted in sheaves on arbitrary infinite-dimensional spaces (<span class="nowrap">{#\infty#}-topoi</span>) has finally been resolved satisfactorily by [Shulman](shulman-2019) in 2019. On the other hand, the computational interpretation of homotopy type theory has involved a reformulation of HoTT called **[cubical](abchfl-2021) [type](angiuli-favonia-harper-2018) [theory](cchm-2017)** that reorganizes the higher-dimensional structure discussed by considering all the points, lines, squares, cubes, hypercubes, and so-on that one can draw in a given type. The computational interpretation of the new cubical type theory can be split into two different conjectures:

![](jms-000S)

![](jms-000T)

The [canonicity conjecture](jms-000S) ensures that terms written in cubical type theory can be thought of as computer programs, and was verified independently by [Huber](huber-2018) and [Angiuli](angiuli-2019) for different variants of cubical type theory. The [decidability conjecture](jms-000T) is no less important, as it is a necessary ingredient to implement a *typechecker* or a *compiler* for a programming language based on cubical type theory.
