Raw LaTeX Code
==========

Pandoc allows raw LaTeX, TeX, and ConTeXt to be included in a document.
Inline TeX commands will be preserved and passed unchanged to the LaTeX and ConTeXt writers.
Thus, for example, you can use LaTeX to include BibTeX citations:
::
  This result was proved in \cite{jones.1967}.

Note that in LaTeX environments, like
::
  \begin{tabular}{|l|l|}\hline
  Age & Frequency \\ \hline
  18--25  & 15 \\
  26--35  & 33 \\
  36--45  & 22 \\ \hline
  \end{tabular}

The material between the begin and end tags will be interpreted as raw LaTeX, not as Markdown.

Inline LaTeX is ignored in output formats other than Markdown, LaTeX, and ConTeXt.
