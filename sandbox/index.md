---
layout: default
title: Davis Advanced RF Technology
published: true
use_math: true
---

Test a display math with equation number:
\begin{equation}
   |\psi_1\rangle = a|0\rangle + b|1\rangle
\end{equation}
Is it O.K.?

Test a display math with equation number:
$$
  \begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
  \end{align}
$$
Is it O.K.?

Test a display math with equation number:
\begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align}
Is it O.K.?

And test a display math without equaltion number:
\begin{align\*}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align\*}
Is it O.K.?



<p class>
{% for post in site.blog limit:6 %}
      » [{{ post.date | date_to_string }}] » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a><br>
{% endfor %}
</p>

![test image test](image/tunable-filter.jpg)
