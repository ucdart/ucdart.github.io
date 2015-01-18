---
layout: default
title: Latex resources
published: true
---

## {{ page.title}}

Refer to the [Wikipedia entry](http://en.wikipedia.org/wiki/LaTeX) for basic information on LaTeX. Some great introductory tutorials on LaTeX include [The Not So Short Introduction to LaTeX2e](http://tobi.oetiker.ch/lshort/lshort.pdf) by [Tobi Oetiker](http://tobi.oetiker.ch/hp/) and the [LATEX Tutorials -- A PRIMER](https://www.tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf) by the Indian Tex User Group. The [LaTeX Wikibook](http://en.wikibooks.org/wiki/LaTeX) is also a great start point. Intermediate level users may find <em>"Guide to LaTeX: Tools and Techniques for Computer Typesetting"</em> by Helmut Kopka and Patrick W. Daly useful.


The following sections list some tips and workarounds that can be useful when you compose a manuscript in LaTeX.

### UC Davis Thesis Template [http://galois.math.ucdavis.edu/UsefulGradInfo/HelpfulAdvice/WritingYourThesis](http://galois.math.ucdavis.edu/UsefulGradInfo/HelpfulAdvice/WritingYourThesis)

<h3> LaTeX editors </h3>
<a href="https://eclipse.org/" target=_blank>Eclipse</a>+TeXlipse is a great combination for LaTeX editing. The PDF viewer that comes with TeXlipse is very fast and supports reverse search. Unfortunately the open source version of Texlipse is no longer being developed. 

<ul>
  <li> Installation:
	<ul>
      <li> Download and unzip Eclipse: Eclipse requires Java VM to run. If you downloaded 64-bit Eclipse, make sure you install 64-bit Java. </li>
      <li> Install Texlipse through software update. An instruction can be found here: <a href="http://texlipse.sourceforge.net/manual/installation.html" target=_blank>http://texlipse.sourceforge.net/manual/installation.html</a> </li>
    </ul>
    <li>The way Eclipse organizes projects is a little bit different than most Windows applications. A project is organized in a folder. In order to open an existing project, you need to go "File->Import->Existing Projects into Workspace". Then select the directory where the project folder resides.</li>
</ul>

<a href="http://texstudio.sourceforge.net/" target=_blank>Texstudio</a> is also a highly recommended editor with a fairly complete set of functionalities. 

<h3> Document Structure </h3>
<h4> Create an empty page </h4>
From: <a href="http://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html">http://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html</a>

<p>It is necessary to use a trick when creating an empty page in Latex. The following code does the job:</p>

<div class="code">
  <pre>
\newpage
\thispagestyle{empty}
\mbox{}
  </pre>
</div>

The major part is \mbox{}, which ensures the existence of an empty page.

The usage of \thispagestyle is \thispagestyle{option}. The option can be:
- plain - Just a plain page number.
- empty - Produces empty heads and feet - no page numbers.
- headings - Puts running headings on each page. The document style specifies what goes in the headings.
- myheadings - You specify what is to go in the heading with the \markboth or the \markright commands.