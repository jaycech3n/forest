---
title: Syntax and models of Cartesian cubical type theory
taxon: reference
author:
- carloangiuli
- Guillaume Brunerie
- Thierry Coquand
- Robert Harper
- Kuen-Bang Hou (Favonia)
- Daniel R. Licata
journal: Mathematical Structures in Computer Science
date: 2021-04-01
---

We present a cubical type theory based on the Cartesian cube category (faces, degeneracies, symmetries, diagonals, but no connections or reversal) with univalent universes, each containing {#\Pi#}, {#\Sigma#}, path, identity, natural number, boolean, suspension, and glue (equivalence extension) types. The type theory includes a syntactic description of a uniform Kan operation, along with judgmental equality rules defining the Kan operation on each type. The Kan operation uses both a different set of generating trivial cofibrations and a different set of generating cofibrations than the Cohen, Coquand, Huber, and Mörtberg (CCHM) model. Next, we describe a constructive model of this type theory in Cartesian cubical sets. We give a mechanized proof, using Agda as the internal language of cubical sets in the style introduced by Orton and Pitts, that glue, {#\Pi#}, {#\Sigma#}, path, identity, boolean, natural number, suspension types, and the universe itself are Kan in this model, and that the universe is univalent. An advantage of this formal approach is that our construction can also be interpreted in a range of other models, including cubical sets on the connections cube category and the De Morgan cube category, as used in the CCHM model, and bicubical sets, as used in directed type theory.
