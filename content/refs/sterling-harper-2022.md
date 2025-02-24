---
title: Sheaf Semantics of Termination-Insensitive Noninterference
taxon: reference
author:
- jonmsterling
- Robert Harper
journal: 7th International Conference on Formal Structures for Computation and Deduction (FSCD 2022)
bookSeries: Leibniz International Proceedings in Informatics (LIPIcs)
---

 We propose a new sheaf semantics for secure information flow over a space of abstract behaviors, based on synthetic domain theory: security classes are open/closed partitions, types are sheaves, and redaction of sensitive information corresponds to restricting a sheaf to a closed subspace. Our security-aware computational model satisfies termination-insensitive noninterference automatically, and therefore constitutes an intrinsic alternative to state of the art extrinsic/relational models of noninterference. Our semantics is the latest application of [Sterling and Harper](sterling-harper-2021)'s recent re-interpretation of phase distinctions and noninterference in programming languages in terms of Artin gluing and topos-theoretic open/closed modalities. Prior applications include [parametricity for ML modules](sterling-harper-2021), the proof of normalization for cubical type theory by [Sterling and Angiuli](sterling-angiuli-2021), and the cost-aware logical framework of [Niu et al](niu-sterling-grodin-harper-2022). In this paper we employ the phase distinction perspective twice: first to reconstruct the syntax and semantics of secure information flow as a lattice of phase distinctions between "higher" and "lower" security, and second to verify the computational adequacy of our sheaf semantics with respect to a version of Abadi et al.’s dependency core calculus to which we have added a construct for declassifying termination channels. 
