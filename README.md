Requires pandoc and 'jupiter lab' installed

1. Start Jupyter lab
2. Open existing or create new Markdown file
3. View this file via "Markdown Preview" in another Jupiter window (after split) 
4. For equations as blocks always use:

```
\begin{equation}
%\label{eq:example_equation}
X = Y + Z
\end{equation}

and refer it with (\ref{eq:example_equation})
```

Note the use of "%\label". It allows to see equation in the Preview window.
Unfortunately (\ref{eq:example_equation}) is visible as (???), however, it is properly shown in pdf. 

Compile file with pandoc_wrapper:

```python pandoc_wrapper example.md -o example.pdf [other pandoc parameters]```

It finds and replaces '%\label' with '\label' and then applies pandoc. All parameters of pandoc_wrapper are propagated to pandoc. 
