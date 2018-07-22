# Pandoc Beamer Metropolis Standout bug

Demonstrates a bug when rendering a beamer presentation with the metropolis theme using pandoc.


## Description

The Metropolis beamer theme supports "standout" frames which are inverted and centered.

Rendering `test.latex` with `pdflatex` directly gives a correctly generated reference document (`out/test.pdf`).

Compiling the equivalent Pandoc markdown file using `pandoc -t beamer test.md -o out/test.pandoc.pdf` gives a buggy output: frames and notes after the standout slide are also affected with the theming which should only apply to the specific slide.


## Environment

```
 % pdflatex --version
pdfTeX 3.14159265-2.6-1.40.17 (TeX Live 2016/Debian)
kpathsea version 6.2.2
Copyright 2016 Han The Thanh (pdfTeX) et al.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the pdfTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the pdfTeX source.
Primary author of pdfTeX: Han The Thanh (pdfTeX) et al.
Compiled with libpng 1.6.28; using libpng 1.6.28
Compiled with zlib 1.2.8; using zlib 1.2.8
Compiled with poppler version 0.48.0

 % pandoc --version
pandoc 2.2.2.1
Compiled with pandoc-types 1.17.5.1, texmath 0.11.0.1, skylighting 0.7.2
Default user data directory: /home/kea/.pandoc
Copyright (C) 2006-2018 John MacFarlane
Web:  http://pandoc.org
This is free software; see the source for copying conditions.
There is no warranty, not even for merchantability or fitness
for a particular purpose.
```
