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
- Ali Afroozeh and Anastasia Izmaylova. **Faster, Practical GLL Parsing**. In Compiler Construction, 24th International Conference, CC 2015, 89-108.

<div>
<ul id="navlist">
<li><a href="#ccAbstract" data-toggle="collapse" data-target="#ccAbstract">Abstract</a></li>
<li><a href="#ccBibtex" data-toggle="collapse" data-target="#ccBibtex">BibTeX</a></li>
<li><a href="http://dx.doi.org/10.1007/978-3-662-46663-6_5">DOI</a></li>
<li><a href="{{ site.url }}/papers/cc15.pdf">PDF</a></li>
<li><a href="https://speakerdeck.com/afroozeh/faster-practical-gll-parsing" target="_blank">Slides</a></li>
</ul>
</div>

<div id="ccAbstract" class="collapse abstract">

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

<div id="ccBibtex" class="collapse bibtex">
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

##### 2012