# `classnotes`
latex for lectures. examples [here](https://web.stanford.edu/~rathi/notes.html).

## about
this is a pdfLaTeX package which is effectively a template for making pretty notes. it comes with preloaded packages/environments/shorthands for things that i do (e.g. math, linguistics, cs, chem) and is primarily built to make writing LaTeX notes in lecture significantly faster & easier.

## basic functionality

### style

there are seven font options which you can pass as you load the package: `human`, `gara`, `transitional`, `dido`, `mech`, `sans`, and `cms`. you can also pass in the `mathfont` option to have the math font match the rest of the text.

if you want slightly more exciting notes you can use the `colors` option, which just redefines the colors of the theorem environments.

### theorems

you can create a theorem-like environment by writing

```latex
\begin{thrm}[Title]
	Content.
\end{thrm}
```

you can create quite a few different environments with this, incl. `eqn`, `lemma`, `corr`, `algo`, `defn`, `example`, `remark`, `claim`, and a substantial amount more. you can also write a `solution` or a two-column proof in a similar way.

### special commands

the package preloads most standard math + cs + linguistics + physics/chem packages. i've defined a reasonable amount of common shorthands which you can find via going through the package; some of these are just things that i prefer (e.g. `\eps = \varepsilon`). i also include auto-sized delimiters like `\p{}` and `\floor{}`.

for linguistics i use forest rather than gb4e. there are a couple fun shorthands like `\phonss` and `\denot[]{}`.
