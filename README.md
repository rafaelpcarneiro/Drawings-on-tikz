# Some Usefull Tikz commands on LaTeX.

## The commands

To start with, if you are just like me, and you just need the basics of the
tikz package, you will find yourself using most of the time the following 
basic commands

```latex
\draw[->] (0,0) -- (1,1);

\shade[inner color = gray!90, outer color = gray!50] (0,0) circle (1cm);

\foreach \x in {0, 60, ..., 360} {
    \draw (\x, 1) circle (0.1cm);
}
```
