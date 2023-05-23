# skak-svg

This project extracts the chess assets from [skak](https://github.com/lehoff/skak) (a package that is behind most chess-related packages in LaTeX) and converts them into SVG format.

The motivation behind this project is that I observe that many chessboard visualization tools use the same set of SVG assets that apparently tries to recreate the skak set but does the job poorly, missing many fine details of the original set. Since that skak set is pretty much the standard for LaTeX, and LaTeX is pretty much the standard for chess documents, I think the community deserves a better (in fact 100% identical) SVG replica of the skak set.

Originally, assets in skak are defined using MetaFont language, which to my knowledge has no straightforward way of converting to other formats. The way this project works is by using pdflatex + [pdf2svg](https://github.com/dawbarton/pdf2svg) to convert an actual output of skak to SVG. The result is then normalized to 100px size, objects are flattened, and finally, the SVG is minified using [svgo](https://github.com/svg/svgo). Some of the pieces initially have their color mask slightly overflown, and those have been manually corrected.

## Preview

![](svg/wk.svg)![](svg/wq.svg)![](svg/wb.svg)![](svg/wn.svg)![](svg/wr.svg)![](svg/wp.svg)

![](svg/bk.svg)![](svg/bq.svg)![](svg/bb.svg)![](svg/bn.svg)![](svg/br.svg)![](svg/bp.svg)

## Credits

This set is originally designed by Piet Tutelaers and modified by Torben Hoffmann.