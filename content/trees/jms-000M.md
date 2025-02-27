---
title: well-pointedness vs. function extensionality
author:
- jonmsterling
date: 2023-01-19T09:16:35-05:00
macros:
- include: base-macros
---

One of the consequences of passing to an intuitionistic set theory is that we must deal with distinctions that did not have significance in the classical setting, such as the **failure of well-pointedness**. In classical set theory, well-pointedness means that a function {#f : A \to B#} is completely determined by its behavior on global elements {#x\in A#} (i.e. functions {#x : 1\to A#}), whereas in intuitionistic set theory this need not hold (indeed, well-pointedness in this sense implies the law of the excluded middle).

In an intuitionistic setting, we must instead consider the composition of {#f : A \to B#} with *arbitrary* functions {#a : I \to A#} in order to fully characterize its behavior. (In some cases, the domains {#I#} of these functions that we must probe by can be drawn from a more restricted class (or even a set) of distinguished set.) In such a setting, therefore, it is convenient to think of a function {#a : I \to A#} as a **generalized element** of {#A#}; then we are saying that {#f : A \to B#} is determined by its behavior on not only global elements but also generalized elements.

The new significance of generalized elements in intuitionistic set theories gives rise to a distinction between two kinds of language: **internal** and **external** language. External language is just ordinary mathematics, where we are explicit about the domains of generalized elements; external language thus allows us to distinguish between a global element and a parameterized element. In contrast, internal language expresses only that which applies to arbitrary generalized elements; internal statements can always be translated mechanically to external ones by explicitly reparameterizing all variable elements as generalized elements (this is called Kripke-Joyal semantics).

For example, even though the external statement of well-pointedness may not hold, the internal one does hold because its externalization is trivial:

> **Internal:** for any functions {#f,g:A\to B#}, if for all {#x:A#} we have {#fx=gx#}, then {#f=g#}.

> **Externalization:** for any set {#I#} and functions {#f,g:I\times A \to B#}, if for all {#i:J\to I#} and {#a:J\to A#} we have {#f \circ \gl{i,a} = g\circ\gl{i,a}#}, then {#f=g#}.

The two statements above are nothing more than the (equivalent) internal and external formulations of the **function extensionality** principle, which is always true in any adequate foundation for mathematics. If the internal statement is read directly as if it were external already, it would be exactly the statement of **well-pointedness**, which is much stronger than function extensionality.
