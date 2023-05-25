# skak-svg

This project extracts the chess assets from [skak](https://github.com/lehoff/skak) (a package that is behind most chess-related packages in LaTeX) and converts them into SVG format.

The motivation behind this project is that I observe that many chessboard visualization tools use the same set of SVG assets that looks a bit similar to the skak set but are poorly drawn, so I decided to create an accurate SVG replica of the skak set. (It later turned out that the poorly drawn set just mentioned has nothing to do with skak, but is based on the `1echecs` font, so I also created [1echecs-svg](https://github.com/MuTsunTsai/1echecs-svg) for it. It's OK; it never hurts to have more chess asset sets.)

Originally, assets in skak are defined using MetaFont language, which to my knowledge has no straightforward way of converting to other formats. The way this project works is by using pdflatex + [pdf2svg](https://github.com/dawbarton/pdf2svg) to convert an actual output of skak to SVG. The result is then normalized to 100px size, objects are flattened, and finally, the SVG is minified using [svgo](https://github.com/svg/svgo). Some of the pieces initially have their color mask slightly overflown, and those have been manually corrected.

Note: For some reason, the contours of white/black queens do not match exactly. The same is true for the knights. I kept the design as it is here.

## Preview

![](svg/wk.svg)![](svg/wq.svg)![](svg/wb.svg)![](svg/wn.svg)![](svg/wr.svg)![](svg/wp.svg)

![](svg/bk.svg)![](svg/bq.svg)![](svg/bb.svg)![](svg/bn.svg)![](svg/br.svg)![](svg/bp.svg)

## Credits

This set is originally designed by Piet Tutelaers and modified by Torben Hoffmann.