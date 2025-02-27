---
title: a wild universal cone from a splitting of the generic element
taxon: construction
tags:
- uf
author:
- jonmsterling
date: 2023-03-14T11:41:03+01:00
macros:
- include: base-macros
- name: CCat
  args: 0
  body: '\mathcal{C}'
  scope: private
---

Let {#\CCat#} be a [wild category](jms-0037), and let {#I:\Ob{\CCat}#} be an object of {#\CCat#} such  that {#\Mor{\alpha}{\Delta I}{\Idn{\CCat}}#} is a [wild natural transformation](jms-0039) from the [constant 0-functor](jms-003D) {#\Mor{\Delta I}{\CCat}{\CCat}#} to the [identity 0-functor](jms-003C) {#\Mor{\Idn{\CCat}}{\CCat}{\CCat}#} on {#\CCat#} for some {#I:\Ob{\CCat}#}. Now let {#r:\Hom{\CCat}{I}{J}#} and {#s:\Hom{\CCat}{J}{I}#} be a section-retraction pair witnessed by {#\eta : s;r = \Idn{I}#}, and let {#\sigma : r;s=\alpha_{I}#} be a splitting of {#\alpha_{I}:\Hom{\CCat}{I}{I}#}. Then we may define a [wild natural transformation](jms-0039) {#\Mor{\beta}{\Delta J}{\Idn{\CCat}}#} and an identification {#\chi : \beta_{J} = \Idn{J}#}.

(This construction is due to [Mike Shulman](https://homotopytypetheory.org/2018/11/26/impredicative-encodings-part-3/).)

{{%proof%}}
Define the component {#\beta_{A}:\Hom{\CCat}{J}{A}#} to be the composite {#s;\alpha_{A}#}; for the wild naturality structure, we fix {#f:\Hom{\CCat}{A}{B}#} to define {#\beta_{f} : \beta_{A};f = \Idn{J};\beta_{B}#} as follows:
{##
\begin{aligned}
\beta_{A};f &= \prn{s;\alpha_{A}};f\\
&= s;\prn{\Idn{A};\alpha_{B}}\\
&= s;\alpha_{B}\\
&= \Idn{J}; \prn{s;\alpha_{B}}\\
&= \Idn{J}; \beta_{B}
\end{aligned}
##}

Next we identify {#\beta_{J}#} with {#\Idn{J}#}. By incoherent naturality, we have {#\alpha_{J};s = \alpha_{I}#}; thus by our splitting of {#\alpha_{I}#} we have {#\alpha_{J};s = r;s#} and hence by postcomposing {#r#} and canceling via {#\eta:s;r=\Idn{I}#} we conclude that {#\alpha_J = r#}. Therefore {#\beta_J=s;\alpha_J=s;r=\Idn{J}#}.

{{%/proof%}}

