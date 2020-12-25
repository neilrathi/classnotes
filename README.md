# `classnotes` package
A LaTeX package designed for LiveTeXing lecture notes.

## Contents
* [About](https://github.com/neilrathi/classnotes#about)
* [Features](https://github.com/neilrathi/classnotes#features)
* [Theorems](https://github.com/neilrathi/classnotes#theorems)
* [Math](https://github.com/neilrathi/classnotes#math)
* [Computer Science](https://github.com/neilrathi/classnotes#computer-science)
* [Linguistics](https://github.com/neilrathi/classnotes#linguistics)
* [Natural Sciences](https://github.com/neilrathi/classnotes#natural-sciences)

## About
The `classnotes` package is a package for LaTeX2e which has pre-loaded packages, environments, and shorthand commands for a variety of fields including math, chemistry, and linguistics. It's useful for anyone who wants to create organized, clear lecture notes which can be easily used for review, and especially helpful for LiveTeXing during lectures. To see the package in use, check out the [classnotes.pdf](https://github.com/neilrathi/classnotes/classnotes.pdf) file in this repository. The rest of the readme is essentially documentation for all of the special commands and features.

To install the package, follow standard procedure for installing a custom `.sty` file. If you're unsure how to do that, check out [this link](https://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te). After loading the package with `usepackage{classnotes}`, you should require minimal setup. Just create a title and author, and then begin your document.

Feel free to use this package for any of your own personal use. If you can, it would be great to reference me as the creator.

You can pass in the `human`, `gara`, `transitional`, `dido`, `mech`, `sans`, and `cms` options to change the document font (the first five refer to their Vox-ATypI categories—Caelacanth, Garamond, Libertinus , TeX Gyre Schola, and Computer Concrete–sans is Latin Modern Sans, and cms is Computer Modern Sans). You can also pass in the `mathfont` option to have the math mode font match the rest of the text.

## Features
The package comes with pre-loaded packages and commands for math, CS, linguistics, and science.

### Theorems
The theorem boxes are created using `mdframed` and `thmtools`. They have a gray background and are generally grouped into three categories. To use one, you can say
```latex
\begin{thrm}[Title]
    Content goes here.
\end{thrm}
```
**Theorem Style**
* Theorems (`thrm`)
* Equations (`eqn`)
* Lemmas (`lemma`)
* Corrolaries (`corr`)
* Algorithms (`algo`)
* Laws (`law`)
* Diagrams (`diagram`)

**Definition Style**
* Definitions (`defn`)
* Examples (`example`)

**Comment Style**
* Remarks (`remark`)
* Hints (`hint`)
* Questions (`question`)
* Claims (`claim`)
* Conjectures (`conj`)
* Propositions (`prop`)

**Proofs:** The `proof` environment is the same as the `amsthm` proof environment, but with a black square for the QED symbol. The `solution` environment is the same, but with *Solution.* instead of *Proof.* in the header. The package also has a two-column proof environment.

### Math
The pre-loaded packages are `amsmath`, `amssymb`, `amsthm`, `amsfonts`, `mathrsfs`, `mathtools`, and `xfrac`.

**General:** The `\mathbb{}` font use the abbreviation `\AA` rather than `\mathbb{AA}`. The `\mathcal{}` font uses `\mcA` rather than `\mathcal{A}`. The command `\phii` outputs φ (varphi), and `\eps` outputs ε.  Some additional generic commands include `\psub` (⊆), `\qeq` (= with ? on top), `\p{}` (parenthesis with automatic resizing), `\floor`, `\ceil`, and `\bvec` (auto-sized delimiters--no more `\left\lfloor x \right\rfloor`), `\thus` (∴), and `\isom` (≃). The package also defines argmin and argmax.

**Trig:** `\sint` and `\sinx` output sinθ and sinx, respectively, and `\sinit` and `\sinix` output sin⁻¹θ and sin⁻¹x. The `\inv` command can replace `^{-1}`, and `\degr` is a quicker way to write °. The package also has cis.

**Logic:** `\nneg` rather than `\mathord{\sim}`, `\is` rather than `\equiv`, `\forA` rather than `\mathord{\forall}`, and `\isE` rather than `\mathord{\exists}`. There is also a `\xor` command (`\oplus`).

**Algebra and NT:** Algebra has `\Gal`, `\Syl`, `\Mat`, `\Hom`, and `\Aut`. For number theory, `\modop{a}{b}{c}` outputs a ≡ b (mod c). There is also `\lcm`, as well as `\cycsum` and `\symsum` (and cycprod and symprod).

### Computer Science
The pre-loaded packages are `algorithm2e`, `listings`, and `stmaryrd`, as well as the TikZ libraries `automata`, `positioning`, and `arrows`. The only additional commands as `\defas` (:=), `\setto` (a more natural ←), and `\bigo` (`\mathcal{O}`).

**Listings:** There are three predefined listing styles--python, java, and C/C++. Use the commannd `\lststyle{a}` instead of `\lstset{style = a}`.

### Linguistics
The pre-loaded packages are `tipa`, `phonrule`, `tikz-dependency`, `forest`, `ot-tableau`, and `linguex`. For phonology, the `\ipa{}` command is the same as `\textipa{}`. The `\ips` and `\ipb` commands automatically place **s**lashes or **b**rackets around the string. `\up` can replace `\super`.

The commands `\phonss`, `\phonsb`, `\phonbs`, and `\phonbb` are all for phonological rules. For example, `\phonsb{p}{p\up h}{C_}` returns /p/ → [pʰ] / C_.

For semantics, the `\lb{}` command places math environment brackets around the input, so it can be easily used when creating semantics tees. The `\lam` command can replace `$\lambda$`. For denotations, `\denot[]{}` puts double brackets around the argument, so `\denot[a]{Alice}` is [[Alice]]ᵃ. `\denotree` does the same, but for tree diagrams.

The package also loads `bussproofs` (for natural-deduction proofs) and `frege` (for *Begriffsschrift*).

### Natural Sciences
The pre-loaded packages are `chemfig` and `mhchem` for chemistry, `physics`, `tensor`, and `circuitikz` for physics, and `siunitx` for units. The `\unt{}` command allows for units to be boxed and typed easily in math mode. In addition, the following non-SI units are provided:
* mile (`\mile`)
* yd (`\yard`)
* ft (`\foot`)
* in (`\inch`)
* lb (`\pound`)
* °F (`\far`)
* c (`\calo`)
* C (`\Calo`)
* atm (`\atm`)
* gal (`\gallon`)
