# Visual-income-distributions Notebooks

## Main report

Report contains the main report notebooks. To compile a pdf, use

`make clean`

then

`make pdf2`

This requires, in addition to an up-to-date Jupyter installation, a LaTeX installation with `pdflatex` available.

There are other `Makefile` targets which was a previous attempts at generating a report (using `nbconvert` to HTML then headless Chrome to PDF). Unfortunately the MathJax library (which converts LaTeX maths notation to symbols) does not load in time for headless Chrome, so the end PDF ends up with notation instead of symbols. Hence the pure LaTeX -> PDF method now.

## Working notebooks

This contains all my other working notebooks. These are a mess, and likely won't run as I modularised the Python code and moved things around, and haven't checked back in again since. To fix.
