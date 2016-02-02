---
layout: base
mustacheSetDelimiter: "{{={| |}=}}"
---

<script src="js/parse-bibtex.js"></script>
<script type="text/javascript" src="js/mustache.min.js"></script>

<script type="text/javascript">
	var publicationsPath = window.location.protocol + "//" + window.location.host + "/" + "publications.bib"
	var thesesPath = window.location.protocol + "//" + window.location.host + "/" + "theses.bib"

	var template = `{{page.mustacheSetDelimiter}}
					<li id="{|paper|}" style="margin-bottom: 10px;">
						<span>{|author|}</span>.
						<span style="font-weight: bold;">{|title|}</span>.
						{|#hasBooktitle|}In <span>{|booktitle|}</span>,{|/hasBooktitle|}
						{|#hasSeries|}<span>{|series|}</span>,{|/hasSeries|}
						{|#hasPages|} pages <span>{|pages|}</span>, {|/hasPages|}
						<span>{|location|}</span>,
						{|#hasPublisher|}<span>{|publisher|}</span>,{|/hasPublisher|}
						{|^hasNote|}<span>{|year|}</span>.{|/hasNote|}
						{|#hasNote|}<span>{|note|}</span>.{|/hasNote|}

						<div>
							<ul id="navlist">
							{|#hasAbstract|}<li><a href="#" data-toggle="collapse" data-target="#{|paper|}Abstract">Abstract</a></li>{|/hasAbstract|}
							<li><a href="#" data-toggle="collapse" data-target="#{|paper|}Bibtex">BibTeX</a></li>
							{|#hasURL|}<li><a href="{|url|}" target="_blank">DOI</a></li>{|/hasURL|}
							{|#hasPreprint|}<li><a href="{|preprint|}" target="_blank">PDF</a></li>{|/hasPreprint|}
							{|#hasSlides|}<li><a href="{|slides|}" target="_blank">Slides</a></li>{|/hasSlides|}
							</ul>
						</div>

						<div id="{|paper|}Abstract" class="collapse abstract" style="border: solid 1px #ccc; border-radius: 10px; padding:10px; background-color: #f5f5f5; margin-top: 10px;">{|&abstract|}</div>
						<div id="{|paper|}Bibtex" class="collapse bibtex"><pre style="margin-top: 10px;">{|bibtex|}</pre></div>
					</li>`

	$(function() {
		jQuery.get(publicationsPath, function(data) {
			$('#publications').html(generate(doParse(data)));
		})
		jQuery.get(thesesPath, function(data) {
			$('#theses').html(generate(doParse(data)));
		})
	})

	function generate(bib) {
		var content = "<ul>"					
		jQuery.each(bib, function(i, val) {
			console.log(val)
			val.paper = i
			val.bibtex = getBibtex(val)
			val.hasBooktitle = isDefined(val.booktitle)
			val.hasPages = isDefined(val.pages)
			val.hasSeries = isDefined(val.series)
			val.hasPublisher = isDefined(val.publisher)
			val.hasSlides = isDefined(val.slides)
			val.hasPreprint = isDefined(val.preprint)
			val.hasURL = isDefined(val.url)
			val.hasNote = isDefined(val.note)
			val.hasAbstract = isDefined(val.abstract)
			val.abstract = addLineBreak(val.abstract)
			val.title = getTitle(val.title)
			content = content.concat(Mustache.render(template, val))
		})
		content = content.concat("</ul>")
		return content
	}

	function getTitle(t) {
		return t.replace(/{(.*)}/g, "$1")
	}

	function isDefined(v) {
		return (typeof v != "undefined") && (v != "")
	}

	function addLineBreak(s) {
		return s.replace(/\n/g, "<br/>")
	}

	function getBibtex(e) {
		return "@" + e.entryType + "{\n" +
			   (isDefined(e.author) ?    "  author={" + e.author + "},\n" : "") + 
			   (isDefined(e.title) ?     "  title={" + e.title + "},\n" : "") +
			   (isDefined(e.booktitle) ? "  booktitle={" + e.booktitle + "},\n" : "") +
			   (isDefined(e.series) ?    "  series={" + e.series + "},\n" : "") +
			   (isDefined(e.year) ?      "  year={"+ e.year + "},\n" : "") + 
			   (isDefined(e.location) ?  "  location={" + e.location + "},\n" : "") +
			   (isDefined(e.pages) ?     "  pages={" + e.pages + "},\n" : "") + 
			   (isDefined(e.numpages) ?  "  numpages={" + e.numpages + "},\n" : "") +
			   (isDefined(e.doi) ?       "  doi={" + e.doi + "},\n" : "") + 
			   (isDefined(e.url) ?       "  url={" + e.url + "},\n" : "") +
			   (isDefined(e.publisher) ? "  publisher={" + e.publisher + "}\n" : "") +
			   (isDefined(e.note) ? "  note={" + e.note + "}\n" : "") +
			   "}\n"
	}
</script>

<h2 class="page-title">Publications</h2>
<div id="publications"></div>

<h2 class="page-title">Theses</h2>
<div id="theses"></div>




