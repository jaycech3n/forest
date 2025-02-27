---
title: A cost-aware logical framework
taxon: reference
author:
- Yue Niu
- jonmsterling
- Harrison Grodin
- Robert Harper
journal: Proceedings of the ACM on Programming Languages
date: 2022-01-01
doi: 10.1145/3462303
---

We present calf, a cost-aware logical framework for studying quantitative aspects of functional programs. Taking inspiration from recent work that reconstructs traditional aspects of programming languages in terms of a modal account of phase distinctions, we argue that the cost structure of programs motivates a phase distinction between intension and extension. Armed with this technology, we contribute a synthetic account of cost structure as a computational effect in which cost-aware programs enjoy an internal noninterference property: input/output behavior cannot depend on cost. As a full-spectrum dependent type theory, calf presents a unified language for programming and specification of both cost and behavior that can be integrated smoothly with existing mathematical libraries available in type theoretic proof assistants. 

We evaluate calf as a general framework for cost analysis by implementing two fundamental techniques for algorithm analysis: the method of recurrence relations and physicist’s method for amortized analysis. We deploy these techniques on a variety of case studies: we prove a tight, closed bound for Euclid’s algorithm, verify the amortized complexity of batched queues, and derive tight, closed bounds for the sequential and parallel complexity of merge sort, all fully mechanized in the Agda proof assistant. Lastly we substantiate the soundness of quantitative reasoning in calf by means of a model construction.
