# "Every Author as First Author"<br>by [Erik D. Demaine](https://erikdemaine.org) and [Martin L. Demaine](http://martindemaine.org)

This repository contains the source code for the following (humorous) paper:

> Erik D. Demaine and Martin L. Demaine.
> "Every author as first author".
> [Proceedings of SIGTBD](http://sigtbd.csail.mit.edu/#archives), 2023.

## [PDF](http://erikdemaine.org/papers/NameStack_SIGTBD2023/paper.pdf)

## [Talk slides](https://github.com/edemaine/author-stack-talk)

## Abstract

We propose a new standard for writing author names on papers
and in bibliographies, which places
*every author as a first author — superimposed*.
This approach enables authors to write papers as true equals,
without any advantage given to whoever's name
happens to come first alphabetically (for example).
We develop the technology for implementing this standard
in LaTeX, BibTeX, and HTML;
show several examples; and discuss further advantages.

## Code

* [namestack.tex](namestack.tex) defines the LaTeX macro `\namestack`
  for overlapping names (or any text) in a stack.
* [stack-natbib.tex](stack-natbib.tex)
  defines additional LaTeX macros for working with author-year bibliographies
  via `natbib.sty`, especially with the following bibliography style:
* [stack-abbrvnat.bst](stack-abbrvnat.bst)
  is a BibTeX style, modifying of
  [abbrvnat.bst](http://tug.ctan.org/tex-archive/macros/latex/contrib/natbib/abbrvnat.bst)
  to stack author names in all entries.
* [stack.html](stack.html) demos name stacks in HTML.
  See [the talk slides](https://github.com/edemaine/author-stack-talk)
  for a more thorough example.

All of the above code (but not the text itself) is distributed under an
[MIT License](https://opensource.org/license/mit/).
Feel free to use them to make your own author stacks!
(with proper attribution)

## Building

To build the paper itself, use `pdflatex` and `bibtex`:

```sh
pdflatex paper
bibtex paper
pdflatex paper
pdflatex paper
```
