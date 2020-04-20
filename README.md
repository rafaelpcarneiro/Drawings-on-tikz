# Some Usefull Tikz commands on LaTeX.


## Purpose of these notes

Here, I intend to keep a list of the most frequently Tikz commands used by me. So, in case I have forgotten them, I can use this list as a faster reminder
of the main commands.


## \draw

Below some self explanatory examples on how to use *draw*.
```latex
\draw[->] (0,0) -- (1,1); % draw an arrow from (0,0) to (1,1) with the shape ->

\draw (0,0) circle (1cm); % draw a circle with origin on (0,0) and with radius of 1cm

\draw (0,0) rectangle (1,1); % draw the following rectangle [0,1] x [0,1] 

\draw (0,0) ellipse (1cm and 2cm); % draw the following rectangle [0,1] x [0,1] 

\draw[step=1cm,color=gray,very thin] (0,0) grid (10,10);

\draw (1,1) node {$x$}; % draw at position (1,1) the letter x
```

Also, when drawing a path you can use the *cycle* command at the end of your path,
ensuring that your path is enclosed. 

Now, one example with the commands we talked above:
```latex
% Axes
\begin{tikzpicture}[scale=2]
    \draw[very thick, ->] (0,0) -- (0,1) node[above right] {$y$};
    \draw[very thick, ->] (0,0) -- (1,0) node[right] {$x$};
    \draw[step=0.2cm, ultra thin, color=gray] (0,0) grid (1,1);

    % Triangle
    \draw[color=gray, ultra thick] (0.2,0.2) -- (0.7,0.4) -- (0.5,0.8) -- cycle;

    % circle
    \draw[fill=red] (0.5,0.5) circle (0.1cm);

    % node
    \draw (0,0) node[below left] {$0$}; % origin of R^2

    % rectangle
    \draw[fill=green] (0.82,0.02) rectangle (0.98,0.18);

\end{tikzpicture}
```

![](Images/example1.png)
