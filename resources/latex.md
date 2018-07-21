---
layout: default
title: UCDart::Resources::Latex
published: true
---

<!--
## {{ page.title}}
-->

Refer to the [Wikipedia entry](http://en.wikipedia.org/wiki/LaTeX) for basic information on LaTeX. Some great introductory tutorials on LaTeX include [The Not So Short Introduction to LaTeX2e](http://tobi.oetiker.ch/lshort/lshort.pdf) by [Tobi Oetiker](http://tobi.oetiker.ch/hp/) and the [LATEX Tutorials -- A PRIMER](https://www.tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf) by the Indian Tex User Group. The [LaTeX Wikibook](http://en.wikibooks.org/wiki/LaTeX) is also a great start point. Intermediate level users may find *"Guide to LaTeX: Tools and Techniques for Computer Typesetting"* by Helmut Kopka and Patrick W. Daly useful. For users of all levels, the [LaTeX Stack Exchange](http://tex.stackexchange.com/) site is always a great resource.

### LaTeX editors

Our group has been using ShareLaTeX, which has now merged with Overleaf, for collaboratively editing LaTeX documents. Compared to a local installation of LaTeX, ShareLaTeX (Overleaf) is not as fast and there is usually noticeable delays in generating the output file. However, its collaboration features, such as shared editing, commenting, and track changes, makes ShareLaTeX a great tool for drafting documents together with a group of people. Being an online tool, it also saves the trouble of installing the LaTeX distribution and ensures that everyone is working with the same setup.

<!--
[Eclipse](https://eclipse.org/)+TeXlipse is a great combination for LaTeX editing. The PDF viewer that comes with TeXlipse is very fast and supports reverse search. Unfortunately the open source version of Texlipse is no longer being developed.

* Installation:
   * Download and unzip Eclipse: Eclipse requires Java VM to run. If you downloaded 64-bit Eclipse, make sure you install 64-bit Java.
   * Install Texlipse through software update. An instruction can be found here: [http://texlipse.sourceforge.net/manual/installation.html](http://texlipse.sourceforge.net/manual/installation.html)

* The way Eclipse organizes projects is a little bit different than most Windows applications. A project is organized in a folder. In order to open an existing project, you need to go "File->Import->Existing Projects into Workspace". Then select the directory where the project folder resides.
-->
When documents have to be edited locally, we use [Texstudio](http://texstudio.sourceforge.net) as the editor and TeX Live as the distribution.

### LaTeX Templates

Perhaps the best way to get started in LaTeX is to use a template.

* [UC Davis dissertation template](http://galois.math.ucdavis.edu/UsefulGradInfo/HelpfulAdvice/WritingYourThesis)
* [IEEE conference templates](http://www.ieee.org/conferences_events/conferences/publishing/templates.html)
* [IEEE journal templates](http://www.ieee.org/publications_standards/publications/authors/author_templates.html)

When you are submitting an academic manuscript, be sure to check the conference or journal website for their designated templates.

### Document Structure

#### Creating an empty page

Source: [http://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html](ttp://nw360.blogspot.com/2007/10/creat-empty-page-in-latex.html)

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

### Width, Length, Height, Indentation, and Margin

Source: [TexExchange](http://tex.stackexchange.com/questions/4239/which-measurement-units-should-one-use-in-latex):

There are no hard-and-fast rules, but here's a short list of guidelines:

* "1em" is a horizontal length and "1ex" a vertical one, so use them accordingly (they are horizontal and vertical arbitrarily, but usually you hear people talk about "1em" is the width of an "m" — usually false — and "1ex" is the height of an "x" — usually true). I usually consider 1em to be about the same size as the font size in points.
* em and ex are relative lengths, so they're better for designing around text; like you say, an indent of 2em will work whether the fontsize is 9pt or 12pt.
* Things that are of fixed size (such as the page size) should be defined with fixed units, of course.
* When things should be relative, it will often make more sense to define them in terms of the page design. For example, width=0.5\linewidth might make more sense than width=5cm for a figure.
* Watch out for the pt unit! In TeX, 1pt is 1/72.27in, whereas the more common "PostScript point" used by most other software is 1/72in which in TeX is 1bp. If you're dealing with other programs and need your lengths exact, use bp or use standard cm or in measurements.

#### Creating equal margins on all sides
Equal margins on all sides of a page can be easily created by using the *geometry* package.

{% highlight latex %}
\usepackage[margin=1in]{geometry}
{% endhighlight %}

#### Paragraph indentation
Put a \noindent before a paragraph to remove the indentation of that paragraph. If you want to remove indentations for all paragraphs, you can put the following in the preamble of the tex file.

{% highlight latex %}
\setlength\parindent{0pt}
{% endhighlight %}

### Text

#### Numbers and Units

In general there should be a space between a number and it's corresponding unit. This space is shorter than a typical space between words. In LaTeX, this can be implement by "number\,unit". Sometimes it is also acceptable to use "number~unit". The "~" creates a typical space, which is longer than the "\,".

A better alternative is to use the *siunitx* package. The manual of the package can be found [here](http://ftp.math.purdue.edu/mirrors/ctan.org/macros/latex/contrib/siunitx/siunitx.pdf)

{% highlight latex %}
%formatting numbers
\num{12345,67890}               %comma represents the decimal point; siunitx also adds the proper spacing for tens and hundreds of thousands
\num{1+-2i}                     %complex numbers
\num{.3e45}                     %with exponentials
\num{1.654 x 2.34 x 3.430}  %multiplication sign

%angles
\ang{10}
\ang{12.3}
\ang{4,5}
\ang{1;2;3}                 %arc format: degree;minute;sec
\ang{;;1} \\

% units
\si{kg.m.s^{-1}}
\si{\kilogram\metre\per\second}
\si{\degreeCelsius}             %degree Celsius

%numbers and units
\SI{100}{\micro\metre}

%list and range
\numlist{10;20;30}
\SIlist{0.13;0.67;0.80}{\milli\metre}
\numrange{10}{20}
\SIrange{0.13}{0.67}{\milli\metre}      %\meter can also be used.
{% endhighlight %}

#### Line spacing in *enumerate* and *itemize* environment
Use the **enumitem** package. The manual for the package can be found [here](http://ctan.mackichan.com/macros/latex/contrib/enumitem/enumitem.pdf)
{% highlight latex %}
\begin{enumerate}[itemsep=-2mm]
    \item xxx
    \item xxx
\end{enumerate}
{% endhighlight %}

#### Custom label in enumerate and itemize environment
Again, use the **enumitem** package. There are several options to choose from: \alph*, \Alph*, \arabic*, \roman*, and
\Roman*.

{% highlight latex %}
\begin{enumerate}[label=\alph* )]
{% endhighlight %}

#### In-line list
Use the *enumerate\** and *itemize\** environments in the **enumitem** package. The *inline* option needs to be enabled in the enumitem package.
{% highlight latex %}
\usepackage[inline]{enumitem}
{% endhighlight %}

#### Indentation in *enumerate* environment
[Source](http://blog.dreasgrech.com/2010/01/indenting-item-in-enumerate-environment.html)
{% highlight latex %}
\newcommand{\indentitem}{\setlength\itemindent{25pt}}

\begin{enumerate}
\item This item is not indented
{\indentitem \item This item is indented}
\item This item is not indented
{\indentitem \item This item is indented}
{\indentitem \item This item is indented}
\item This item is not indented
\end{enumerate}
{% endhighlight %}

#### Hyphen, En Dash, Em Dash, ...

{% highlight latex %}
-              %Hypen: refer to http://owl.english.purdue.edu/owl/resource/576/01/
--             % En Dash: for indicating a closed range of values, e.g. 1987-1992, or a relationship, e.g. "Score: 96-100"
---            % Em Dash: used to separate or shift thoughts midstream through a sentence
{% endhighlight %}

For more information on the use of hyphen, en dash, and em dash, refer to [http://thegrammargang.blogspot.com/2012/07/dash-it-all-whats-point-of-hypen-help.html](http://thegrammargang.blogspot.com/2012/07/dash-it-all-whats-point-of-hypen-help.html)

#### Strike through text
Striking through texts using a horizontal line can be achieved by using the *soul* package.
{% highlight latex %}
\usepackage{soul}
...
\st{text to strike through}
{% endhighlight %}

### Math

#### Upright bold symbols

By default, the \mathbf command does not generate upright bold font for Greek alphabets, which are often used to denote matrices. Use the *bm* package for this purpose.
{% highlight latex %}
\usepackage{bm}
...
$\bm{\Phi}$
{% endhighlight %}

#### Center-aligned equations
Use the gather *environment* (included in the *amsmath* package) to generate a set of equations that are center aligned.

Using multiple \[ \] can generate center aligned equations without equation numbers.

### Tables

#### Multi-page Tables

Use package *longtable*. [Here](http://users.sdsc.edu/~ssmallen/latex/longtable.html) is one example.

#### Adding notes to table

Use the *threeparttable* package. Below is an example. Source: http://tex.stackexchange.com/questions/12676/add-notes-under-the-table

{% highlight latex %}
\begin{table}
  \begin{threeparttable}
    \caption{Sample ANOVA table}
     \begin{tabular}{lllll}
      \toprule
        Stubhead & \( df \) & \( f \) & \( \eta \) & \( p \) \tnote{$\dagger$} \\
      \midrule
        & \multicolumn{4}{c}{Spanning text} \\
        Row 1 & 1 & 0.67 & 0.55 & 0.41 \\
        Row 2 & 2 & 0.02 & 0.01 & 0.39 \\
        Row 3 & 3 & 0.15 & 0.33 & 0.34 \\
        Row 4 & 4 & 1.00 & 0.76 & 0.54 \\
      \bottomrule
    \end{tabular}
    \begin{tablenotes}
      \small                    %optional
      \item [$\dagger$] This is where authors provide additional information about
      the data, including whatever notes are needed.
    \end{tablenotes}
  \end{threeparttable}
\end{table}
{% endhighlight %}

### Figures

#### Inserting Figures

The following code works both for LaTeX and pdfLaTeX for inserting figures.

{% highlight latex %}
\begin{figure}[t]
    \centering
        \includegraphics{FigureFileName}
        \caption{Caption}
        \label{fig:label}
\end{figure}
{% endhighlight %}

Note that an extension for the figure file name is not specified. When using pdfLaTeX, save the file with extension .pdf; when using LaTeX, save the file with extension .eps.

Also it is very important that the \label command be placed **immediately after** the \caption command. Otherwise the \ref command would reference the last reference-able object, which is often the section label or the previous figure. Putting the \label command consistently before the \caption can be a dangerous practice that may completely disrupt your figure references.

#### Changing Font Size in Caption
Use the *caption* package.
{% highlight latex %}
\usepackage[font={small,it}]{caption}           % font size can be "large, small, footnotesize, scriptsize,etc"
{% endhighlight %}

#### Wrap Text Around Figures
Use the *wrapfig* package.

{% highlight latex %}
\begin{wrapfigure}{r}{2.4in}            %"r" indicates right aligned. It is also important that the width be set to the actual width of the figure
   \begin{center}
     \includegraphics{figure}
   \end{center}
   \caption{Caption.}
\end{wrapfigure}
{% endhighlight %}

#### Adjusting the space around figures/floats
Direct application of the *wrapfigure* environment often results in excessive white space above the figures. The following trick can be used to adjust the spacing.

{% highlight latex %}

\begingroup
\setlength\intextsep{-3pt}

\begin{wrapfigure}{r}{3.2 in}            %"r" indicates right aligned
   \begin{center}
     \includegraphics{trends}
   \end{center}
   \caption{The trend and projection of chip-to-chip communication data
   bandwidth and the number of pins over the time. Data from D. Huang, IEEE HSD
   Workshop, Santa Fe, 2011~\cite{huang2011}}
   \label{fig:trends}
\end{wrapfigure}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

\endgroup
{% endhighlight %}

Note that the group includes the wrapped figure and some texts. The text must exceed the vertical span of the figure, otherwise the following paragraph will intrude into the figure.

#### Side-by-side Figures

{% highlight latex %}
\begin{figure}
\centering
\begin{minipage}{.5\textwidth}          %alternatively, this could be //\minipage{0.5\textwidth}//
    \centering
    \includegraphics[width=.85\linewidth]{figure1}
    \captionof{figure}{Caption 1.}
    \label{fig:1l}
\end{minipage}                          %alternatively, this could be //\endminipage//
\hfill                                      % distribute the two minipages evenly. This has the effect of creating a small gap between the figures if set properly.
\begin{minipage}{.5\textwidth}          %[IMPORTANT]: there shouldn't be a blank line between the two //minipage// environments
    \centering
    \includegraphics[width=.8\linewidth]{figure2}
    \captionof{figure}{Caption 2.}
    \label{fig:2}
\end{minipage}
\end{figure}
{% endhighlight %}

#### Figure in tables

{% highlight latex %}
We can insert figures in tables (see example below, from http://texblog.org/2008/02/04/placing-graphicsimages-inside-a-table/), however the figures placed in tables won't get numbered and won't appear in the automatically generated list of figures.

\begin{table}[ht]
    \caption{A table arranging images}
    \centering
    \begin{tabular}{cc}
        \includegraphics[scale=1]{graphic1} &   \includegraphics[scale=1]{graphic2}\\
        \newline
        \includegraphics[scale=1]{graphic3}&\includegraphics[scale=1]{graphic4}\\
    \end{tabular}
    \label{tab:gt}
\end{table}
{% endhighlight %}

### Bibliography

#### Hiding references

The *\nobibliography{bibfile}* command allows you to generate citations via Bibtex without creating a “References” section at the end of your document. This command is enabled by the *bibentry* package.

### Useful references on LaTeX

[Math into LaTeX](http://ctan.math.washington.edu/tex-archive/info/mil/mil.pdf)
[The Comprehensive LATEX Symbol List](http://tug.ctan.org/info/symbols/comprehensive/symbols-a4.pdf)
