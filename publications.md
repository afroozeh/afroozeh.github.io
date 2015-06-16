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

##### 2015
- Ali Afroozeh and Anastasia Izmaylova. **Faster, Practical GLL Parsing**. 
In Compiler Construction, 24th International Conference, CC 2015, LNCS 9031, Springer, pp 89-108.

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

##### 2013
- Ali Afroozeh, Mark van den Brand, Adrian Johnstone, Elizabeth Scott and Jurgen Vinju. **Safe Specification of Operator Precedence Rules**. 
In Software Language Engineering, 6th International Conference, SLE 2013, LNCS 8225, Springer, pp 137-156.

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


##### 2012