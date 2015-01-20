---
layout: default
title: Latex resources
published: true
---

## {{ page.title}}

Refer to the [Wikipedia entry](http://en.wikipedia.org/wiki/LaTeX) for basic information on LaTeX. Some great introductory tutorials on LaTeX include [The Not So Short Introduction to LaTeX2e](http://tobi.oetiker.ch/lshort/lshort.pdf) by [Tobi Oetiker](http://tobi.oetiker.ch/hp/) and the [LATEX Tutorials -- A PRIMER](https://www.tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf) by the Indian Tex User Group. The [LaTeX Wikibook](http://en.wikibooks.org/wiki/LaTeX) is also a great start point. Intermediate level users may find *"Guide to LaTeX: Tools and Techniques for Computer Typesetting"* by Helmut Kopka and Patrick W. Daly useful.

### LaTeX editors 

[Eclipse](https://eclipse.org/)+TeXlipse is a great combination for LaTeX editing. The PDF viewer that comes with TeXlipse is very fast and supports reverse search. Unfortunately the open source version of Texlipse is no longer being developed. 

* Installation:
   * Download and unzip Eclipse: Eclipse requires Java VM to run. If you downloaded 64-bit Eclipse, make sure you install 64-bit Java.
   * Install Texlipse through software update. An instruction can be found here: <a href="http://texlipse.sourceforge.net/manual/installation.html" target=_blank>http://texlipse.sourceforge.net/manual/installation.html</a>

* The way Eclipse organizes projects is a little bit different than most Windows applications. A project is organized in a folder. In order to open an existing project, you need to go "File->Import->Existing Projects into Workspace". Then select the directory where the project folder resides.

[Texstudio](http://texstudio.sourceforge.net) is also a highly recommended editor with a fairly complete set of functionalities. 

### LaTeX Templates

Perhaps the best way to get started in LaTeX is to use a template. 

* [UC Davis dissertation template](http://galois.math.ucdavis.edu/UsefulGradInfo/HelpfulAdvice/WritingYourThesis)
* [IEEE conference templates](http://www.ieee.org/conferences_events/conferences/publishing/templates.html)
* [IEEE journal templates](http://www.ieee.org/publications_standards/publications/authors/author_templates.html)

Be sure to check the conference or journal website for thier 

### Document Structure

#### Create an empty page

From: [http://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html](ttp://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html)

It is necessary to use a trick when creating an empty page in Latex. The following code does the job:

{% highlight latex %}
\newpage
\thispagestyle{empty}
\mbox{}
{% endhighlight %}

The major part is \mbox{}, which ensures the existence of an empty page.

The usage of \thispagestyle is \thispagestyle{option}. The option can be:

* plain - Just a plain page number.
* empty - Produces empty heads and feet - no page numbers.
* headings - Puts running headings on each page. The document style specifies what goes in the headings.
* myheadings - You specify what is to go in the heading with the \markboth or the \markright commands.

#### Width, Length, Height, and Margin

Source: [TexExchange](http://tex.stackexchange.com/questions/4239/which-measurement-units-should-one-use-in-latex):

There are no hard-and-fast rules, but here's a short list of guidelines:

* "1em" is a horizontal length and "1ex" a vertical one, so use them accordingly (they are horizontal and vertical arbitrarily, but usually you hear people talk about "1em" is the width of an "m" — usually false — and "1ex" is the height of an "x" — usually true). I usually consider 1em to be about the same size as the font size in points.
* em and ex are relative lengths, so they're better for designing around text; like you say, an indent of 2em will work whether the fontsize is 9pt or 12pt.
* Things that are of fixed size (such as the page size) should be defined with fixed units, of course.
* When things should be relative, it will often make more sense to define them in terms of the page design. For example, width=0.5\linewidth might make more sense than width=5cm for a figure.
* Watch out for the pt unit! In TeX, 1pt is 1/72.27in, whereas the more common "PostScript point" used by most other software is 1/72in which in TeX is 1bp. If you're dealing with other programs and need your lengths exact, use bp or use standard cm or in measurements.
