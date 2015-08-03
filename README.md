attention -- Paying attention to the consistency of your work
=============================================================

The package wraps environments like `figure` and `table` to pay attention to
the usage of `\caption` and `\label`. If they are missing a warning will be
shown.

Installation
------------

Either clone repository to your local texmf-tree or the document's directory:
```
$ cd ~/texmf/tex/latex
$ git clone https://github.com/8ware/latex-attention.git
```
or
```
$ git clone https://github.com/8ware/latex-attention.git
$ ln -s latex-attention/attention.sty .
```

Usage
-----

```latex
\usepackage{attention}
```

Dependencies
------------

* `ifthen` package
* `todonotes` package

Licence
-------

The sources are licenced under the GPL V3 (see [[LICENCE][]]!)

