---
---

<html>

<head>
	<title>Ali Afroozeh</title>
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"/></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
	<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
	<link rel="stylesheet" href="style.css"/>
	<link rel="stylesheet" href="page.css"/>
</head>

<body class="markdown-body"  markdown='1'>

<div id="navcontainer">
<ul id="navlist">
<li><a href="{{ site.baseurl }}/index.html">Home</a></li>
<li><a href="{{ site.baseurl }}/publications.html">Publications</a></li>
<li><a href="{{ site.baseurl }}/projects.html">Projects</a></li>
<li><a href="{{ site.baseurl }}/presentations.html">Presentations</a></li>
<li><a href="{{ site.baseurl }}/contact.html">Contact</a></li>
</ul>
</div>


## Publications

- Ali Afroozeh and Anastasia Izmaylova. **One Parser to Rule Them All**. 
In Proceedings of the 2015 ACM International Symposium on New Ideas, New Paradigms, and Reflections on Programming & Software, Onward!'15, pages 193-212. ACM, 2015.

<div>
<ul id="navlist">
<li><a href="#onward15Abstract" data-toggle="collapse" data-target="#onward15Abstract">Abstract</a></li>
<li><a href="#onward15Bibtex" data-toggle="collapse" data-target="#onward15Bibtex">BibTeX</a></li>
<li><a href="http://dx.doi.org/10.1145/2814228.2814242">DOI</a></li>
<li><a href="https://cdn.rawgit.com/iguana-parser/papers/master/onward15.pdf">PDF</a></li>
<li><a href="" target="">Slides</a></li>
</ul>
</div>

<div id="onward15Abstract" class="collapse abstract">

Despite the long history of research in parsing, constructing parsers for real programming languages remains a difficult and painful task. In the last decades, different parser generators emerged to allow the construction of parsers from a BNF-like specification. However, still today, many parsers are handwritten, or are only partly generated, and include various hacks to deal with different peculiarities in programming languages. The main problem is that current declarative syntax definition techniques are based on pure context-free grammars, while many constructs found in programming languages require context information.<br/>

In this paper we propose a parsing framework that embraces context information in its core. Our framework is based on data-dependent grammars, which extend context-free grammars with arbitrary computation, variable binding and constraints. We present an implementation of our framework on top of the Generalized LL (GLL) parsing algorithm, and show how common idioms in syntax of programming languages such as (1) lexical disambiguation filters, (2) operator precedence, (3) indentation-sensitive rules, and (4) conditional preprocessor directives can be mapped to data-dependent grammars. We demonstrate the initial experience with our framework, by parsing more than 20000 Java, C#, Haskell, and OCaml source files.<br/>
</div>

<div id="onward15Bibtex" class="collapse bibtex">
<pre>
@inproceedings{
 author={Afroozeh, Ali and Izmaylova, Anastasia},
 title = {One Parser to Rule Them All},
 booktitle = {Proceedings of the 2015 ACM International Symposium on New Ideas, New Paradigms, and Reflections on Programming & Software},
 series = {Onward! 2015},
 year = {2015},
 location = {Pittsburgh, PA, USA},
 pages = {193--212},
 numpages = {20},
 url = {http://dx.doi.org/10.1145/2814228.2814242},
 doi = {10.1145/2814228.2814242},
 acmid = {2814242},
 publisher = {ACM},
 address = {New York, NY, USA},
 keywords = {Parsing, data-dependent grammars, GLL, disambiguation, operator precedence, offside rule, preprocessor directives,  scannerless parsing, context-aware scanning},
} 

</pre>
</div>

- Ali Afroozeh and Anastasia Izmaylova. **Faster, Practical GLL Parsing**. 
In Compiler Construction, 24th International Conference, CC 2015, LNCS 9031, pages 89-108. Springer, 2015.

<div>
<ul id="navlist">
<li><a href="#cc15Abstract" data-toggle="collapse" data-target="#cc15Abstract">Abstract</a></li>
<li><a href="#cc15Bibtex" data-toggle="collapse" data-target="#cc15Bibtex">BibTeX</a></li>
<li><a href="http://dx.doi.org/10.1007/978-3-662-46663-6_5">DOI</a></li>
<li><a href="{{ site.url }}/papers/cc15.pdf">PDF</a></li>
<li><a href="https://speakerdeck.com/afroozeh/faster-practical-gll-parsing" target="_blank">Slides</a></li>
</ul>
</div>

<div id="cc15Abstract" class="collapse abstract">

Generalized LL (GLL) parsing is an extension of recursive-descent (RD)
parsing that supports all context-free grammars in cubic time and space.
GLL parsers have the direct relationship with the 
grammar that RD parsers have, and therefore, compared to GLR, are easier to 
understand, debug, and extend. This makes GLL parsing attractive
for parsing programming languages.<br/>

In this paper we propose a more efficient Graph-Structured Stack (GSS)
for GLL parsing that leads to significant performance improvement.
We also discuss a number of optimizations that
further improve the performance of GLL. Finally, for practical scannerless
parsing of programming languages, we show how common lexical 
disambiguation filters can be integrated in GLL parsing.<br/> 

Our new formulation of GLL parsing is implemented as part of the Iguana 
parsing framework. We evaluate the effectiveness of our approach
using a highly-ambiguous grammar and grammars of real 
programming languages. Our results, compared to the original GLL, 
show a speedup factor of 10 on the highly-ambiguous grammar, and a 
speedup factor of 1.5, 1.7, and 5.2 on the grammars of Java, C#, and OCaml, 
respectively.
</div>

<div id="cc15Bibtex" class="collapse bibtex">
<pre>
@incollection{
	year={2015},
	isbn={978-3-662-46662-9},
	booktitle={Compiler Construction},
	volume={9031},
	series={Lecture Notes in Computer Science},
	editor={Franke, Björn},
	doi={10.1007/978-3-662-46663-6_5},
	title={Faster, Practical GLL Parsing},
	url={http://dx.doi.org/10.1007/978-3-662-46663-6_5},
	publisher={Springer Berlin Heidelberg},
	author={Afroozeh, Ali and Izmaylova, Anastasia},
	pages={89-108},
	language={English}
}
</pre>
</div>

- Ali Afroozeh, Mark van den Brand, Adrian Johnstone, Elizabeth Scott and Jurgen Vinju. **Safe Specification of Operator Precedence Rules**. 
In Software Language Engineering, 6th International Conference, SLE 2013, LNCS 8225, pages 137-156. Springer, 2013.

<div>
<ul id="navlist">
<li><a href="#sle13Abstract" data-toggle="collapse" data-target="#sle13Abstract">Abstract</a></li>
<li><a href="#sle13Bibtex" data-toggle="collapse" data-target="#sle13Bibtex">BibTeX</a></li>
<li><a href="http://dx.doi.org/10.1007/978-3-319-02654-1_8">DOI</a></li>
<li><a href="{{ site.url }}/papers/sle13.pdf">PDF</a></li>
<li><a href="" target="_blank">Slides</a></li>
</ul>
</div>

<div id="sle13Abstract" class="collapse abstract">
In this paper we present an approach to specifying operator precedence 
based on declarative disambiguation constructs and an implementation mechanism 
based on grammar rewriting. We identify a problem with existing generalized 
context-free parsing and disambiguation technology: generating a correct parser 
for a language such as OCaml using declarative precedence specification is not 
possible without resorting to some manual grammar transformation. 
Our approach provides a fully declarative solution to operator precedence specification
for context-free grammars, is independent of any parsing technology, and is safe 
in that it guarantees that the language of the resulting grammar will be the same as the
language of the specification grammar. 
We evaluate our new approach by specifying the precedence rules from the OCaml reference 
manual against the highly ambiguous reference grammar and validate the output of our generated parser.
</div>

<div id="sle13Bibtex" class="collapse bibtex">
<pre>
@incollection{
	year={2013},
	isbn={978-3-319-02653-4},
	booktitle={Software Language Engineering},
	volume={8225},
	series={Lecture Notes in Computer Science},
	editor={Erwig, Martin and Paige, RichardF. and Van Wyk, Eric},
	doi={10.1007/978-3-319-02654-1_8},
	title={Safe Specification of Operator Precedence Rules},
	url={http://dx.doi.org/10.1007/978-3-319-02654-1_8},
	publisher={Springer International Publishing},
	author={Afroozeh, Ali and van den Brand, Mark and Johnstone, Adrian and Scott, Elizabeth and Vinju, Jurgen},
	pages={137-156},
	language={English}
}
</pre>
</div>


## Theses

- Ali Afroozeh. **GText: A Language Workbench based on GLL and Term Rewriting**.
Master's Thesis, Eindhoven University of Technology, 2012.

<div>
<ul id="navlist">
<li><a href="#mscThesisAbstract" data-toggle="collapse" data-target="#mscThesisAbstract">Abstract</a></li>
<li><a href="http://alexandria.tue.nl/extra1/afstversl/wsk-i/afroozeh2012.pdf">PDF</a></li>
<li><a href="https://speakerdeck.com/afroozeh/gtext-a-language-workbench-based-on-gll-and-term-rewriting" target="_blank">Slides</a></li>
</ul>
</div>

<div id="mscThesisAbstract" class="collapse abstract">

One of the main difficulties in developing domain-specific languages is the use of
deterministic parsing technologies in language workbenches. These deterministic
parsers do not naturally support modularity, and impose restrictions on
defining the grammar of a language. For example, LL(k) parsers cannot deal with
left recursion or ambiguities, which have to be removed by rewriting the
grammar. These modifications usually lead to a grammar definition which is not
readable and may cause maintenance problems. More importantly, the parse trees
from a modified grammar may be significantly different from the ones of the
original, ambiguous grammar. This may cause problems in processing parse trees,
for example, for mapping to EMF models.

In this thesis, we present a new language workbench based on the GLL parsing
algorithm. GLL is able to parse the full class of context-free grammars without
any limitation and thus inherently supports modularity. Being a generalized
parser, GLL produces a parse forest containing all the ambiguities. Our
disambiguation method is based on pattern matching and rewriting within the
resulting parse forest. One of the motivations for our disambiguation mechanism
is solving hard parsing problems such as language embeddings and extensions. In
addition, we present an error reporting mechanism for GLL-based parsers, an
Eclipse plugin for developing new languages, and facilities for the mapping of ambiguous, 
complex concrete syntax to EMF models.
</div>

