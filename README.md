# Quick Start

If your main file is `mypaper.tex`:

    $ curl -O https://raw.github.com/ransford/pdflatex-makefile/master/Makefile.include
    $ cat > Makefile
    TARGET=mypaper
    include Makefile.include

# Features

Simple Makefile for typesetting papers using pdflatex.

Features:

* Simple to use: just set `TARGET=<yourpaper>` and `include Makefile.include`.
  See the `example/` directory for a usage example.
* Supports multiple targets: set `TARGETS=paper1 paper2` instead of `TARGET`.
* Calculates dependencies sanely.  Detects changes to included .tex and .bib
  files and rebuilds when appropriate.
* Detects your revision control system (svn, git, hg) and defines a `\Revision`
  command you can use in your LaTeX markup to include a current revision
  identifier.  Useful for circulating drafts for comment.
* `make view` opens your typeset document.
* Distills a camera-ready PDF (with fonts embedded): `make distill`
* To generate a draft with the revision number in its filename (to pass
  around), use `make snapshot`.
* Vector graphics in the `svg/` directory are being compiled into pdf+LaTeX using inkscape
