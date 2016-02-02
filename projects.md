---
layout: base
---

<h2 class="page-title">Projects</h2>

- **Iguana parsing framework:** <a href="http://iguana-parser.github.io">Iguana</a> 
Iguana is a parsing framework based on data-dependent grammars. Data-dependent 
grammars extend context free grammars with arbitrary computation, variable 
binding, and constraints. These powerful features enable construction of parsers 
for context-sensitive languages. We also use data-dependent grammars as a layer 
to implement different disambiguation constructs such as operator precedence.

- **Meerkat Parser Combinators:** <a href="http://meerkat-parser.github.io">Meerkat</a> 
is a general parser combinator library written in Scala, that combines the 
flexibility of traditional, monadic parser combinators and the expressivity 
and worst-case performance guarantees of state-of-the-art general parsing 
algorithms, such as GLL and GLR. Using the Meerkat library, it is possible 
to directly encode any context-free grammar, including the ones with direct and 
indirect left recursion, in Scala. Meerkat parsers support ambiguity, by producing 
a parse forest in cubic time and space, and can behave nearly linear on grammars 
of real programming languages.
