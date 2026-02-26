# Object Oriented Constraint Programming

This repo is based on that of the College Doctoral de Bretagne (see below)

Main folders are `./Context` and `./Contributions/`.
Each Chapter Folder has a main .tex file, and two sub-folders for text and figures.

## quick guide
to update `./main.pdf` edit the `./main.tex` file and run `make`.


# Progress
## Context:
- [ ] Chapter 0: Introduction
- [ ] Chapter 1: MDE
	- [x] UML
    	- [x] MOF
    	- [x] Class
    	- [x] Object 
	- [ ] OCL
    	- [x] by example
    	- [ ] operation summary
    	- [x] typing OCL expressions
    	- [ ] OCL Metamodel
  	- [x] SotA
    	- [x] EMF
    	- [x] ATL
- [ ] Chapter 2: CSP
  - [x] CSP
  - [ ] ~~Propagation~~
  - [x] Globals
    - [x] Examples
    - [x] Example Propagation
    - [ ] DPLL & Simplex
  - [ ] SotA
    - [ ] Choco (& others)
    - [ ] Eclipse (& SWI-prolog)
    - [ ] SAT4j (&Cassowary)
- [ ] Chapter 3: Problem
  - [x] Model Search
  - [ ] SotA
    - [x] ATLc (QVTc (Grimm))
    - [ ] EMFtoCSP (OCL\#)
    - [x] Alloy & Kodkod (OCLsolve)
    - [ ] ~~QVTc~~
    - [ ] ~~Grimm~~
    - [ ] ~~OCL\#~~
    - [ ] ~~OCLsolve~~

## Contrib:
- [x] Chapter 4: var
  - [x] RMS Problem
  - [x] Denoting Vars
  - [x] Refactoring Expressions
  - [ ] Experimentation : Refactoring RMS
  - [ ] Discussions
- [ ] Chapter 5: UML CSP
  - [x] Base Encoding
  - [ ] Enumerated Encoding (References)
  - [ ] ~~3-valued Boolean Encoding (optional data)~~
  - [ ] Reference Types
    - [ ] ~~Containment~~
    - [ ] Opposite
  - [x] Collection Types
    - [x] Sequence
    - [x] Set
    - [x] Bag
    - [x] OrderedSet
  - [ ] Comparison to Alloy and EMF2CSP
- [ ] Chapter 6: Nav CSP
  - [x] Base Model
  - [ ] ~~Enumerated Model~~
  - [ ] ~~Closure~~
  - [ ] Experimentation : Subset Sum
    - [x] n-depth Our Method
    - [ ] n-depth Alloy
    - [ ] ~~Closure our Method~~
    - [ ] ~~Closure Alloy~~
  - [ ] Comparison to Alloy and EMF2CSP
- [ ] Chapter 7: OCL CSP
  - [x] Int and Bool OP
    - [x] 1..1 Int and Bool
      - [ ] ~~models~~
      - [x] text
    - [x] 0..1 Bool
      - [x] models
      - [x] text
    - [x] 0..1 Int
      - [ ] ~~models~~
      - [x] text
  - [ ] ~~Iterate~~
    - [ ] ~~2 int model~~
    - [ ] ~~2 bool model~~
    - [ ] ~~2 collection~~
  - [ ] Col to Int OP
    - [x] models
    - [ ] text
  - [ ] Col to Bool OP
    - [x] models
      - [ ] forall <- many valued logic problem
    - [ ] text
  - [ ] Col to Col OP
    - [x] models
    - [ ] text
  - [x] Col Type Casting
    - [x] models
    - [x] text
    - [ ] experimentation: Zoo
  - [ ] Ordered Col OPs
    - [x] models
    - [ ] text
  - [ ] Unordered Col OPs
    - [x] models
    - [ ] text
- [ ] ~~Chapter 8: Comparison with Related Work~~
- [ ] Chapter 9: Discussions
  - [ ] Summary: Comparison with related work
  - [ ] OOCP Benchmark suite
  - [ ] Search Strategy
  - [ ] Sequence/String Variables to replace encoding and global constraints
- [ ] Chapter 10: Conclusion
# ![(UK flag)](https://upload.wikimedia.org/wikipedia/en/thumb/a/ae/Flag_of_the_United_Kingdom.svg/50px-Flag_of_the_United_Kingdom.svg.png) Thesis template for Collège Doctoral de Bretagne

*English explanations*

This repository contains a template for the thesis manuscript supporting all doctoral schools of the [Collège Doctoral de Bretagne](https://www.doctorat-bretagne.fr/en).

<!-- 
The main goal of this template is to provide both front and back covers of the thesis manuscript entirely written in latex.
While the manuscript covers must follow the rules of CDL, the internal layout of the content is more flexible.
The content layout provided in this template is therefore given as an exemple rather than as a  mandatory framework.


#### Structure of the repository

- `main.tex` contains the backbone structure of the document, no content is present in this file
- `these-dbl.cls` contains the package dependencies, bibliography parameters including citation style and overall layout specifications including both front and back cover layouts
- `Couverture-these/pagedegarde.tex` contains the variables that must be filled by the author to complete the front cover, these variables are used in `\maketitle` redefined in `these-dbl.cls`
- `Couverture-these/resume.tex` contains the variables that must be filled by the author to complete the back cover, these variables are used in the macros defined in `these-dbl.cls`
- The `Makefile` helps you compile the latex and bibliography into a pdf (details below)
- The rest of the directories each contain one chapter of the document


#### Fill the front and back cover

The front cover details must be provided by filling the variables in `Couverture-these/pagedegarde.tex`.
The lines calling the `\ecoledoctorale{}` and `\etablissement{}` (i.e., institution) commands must be modified to adapt the covers to the doctoral school and institution(s) delivering the diplome (by default set to MathSTIC and Université de Rennes 1, respectively).
The file `Couverture-these/README.md` lists the supported doctoral schools and institutions, and contains links pointing to lists of domains and labs/faculties, for each doctoral school, that are needed to fill the front cover (commands `\spec{}` and `\uniterecherche{}`).
Modifying the front cover layout defined in `these-dbl.cls` should only be necessary to preserve the original layout using a few `\vspace` after filling the front cover (e.g., domain, jury section).

The back cover variables that must be filled are in `Couverture-these/resume.tex`.

-->
#### Dependencies

A LaTeX distribution such as texlive is necessary in order to compile your document. Please note some necessary packages are not directly included in a base texlive installation.

Required additional packages:

- Fedora (install using `dnf install`)
	- texlive-abstract
	- texlive-wallpaper
- Other distributions
	- TODO (contributions welcome)


#### Compile latex into pdf

A `Makefile` is provided to help you compile your document. It uses `pdflatex` and`biber` to generate the pdf file and can display it by using `evince` on Linux or `open` on MacOS.

Compile your document (local version) with `pdflatex/biber`:

	make

Compile the whole document (including section masked locally):

	make full

Display the generated pdf:

	make viewpdf

Remove all generated files, pdf included:

	make clean
<!--
#### CI/CD (Gitlab only)

This repository is able to automatically compile the LaTeX document when a new change is submitted.
To activate the auto compilation of the document:

- Settings -> General -> Visibility, project features, permissions -> Enable CI/CD
- (on the https://gitlab.com instance) Settings -> CI/CD -> Enable shared runners for this project

The compiled document should be available at this URL: <repository url>-/jobs/artifacts/master/raw/main.pdf?job=building-latex-master

Ex: https://gitlab.com/ed-matisse/latex-template/-/jobs/artifacts/master/raw/main.pdf?job=building-latex-master


#### Particularities of a multilanguage document

The list of used languages is defined in `these-dbl.cls` where the package `babel` is imported.
As the back cover contains both French and English, it is necessary to keep at least both these languages in the list.
Use `\selectlanguage{x}` (where x is `french` or `english`) to switch language after its usage.

If the main language of your document is English, you must apply the following changes to the provided template:

- replace `\selectlanguage{french}` by `\selectlanguage{english}` in `main.tex`
- edit line 488 of `these-dbl.cls` to replace `Partie` by `Part` in the headers
- include a summary in French of at least 4 pages


### Change the content font

The required font for the covers is Arial but you can use another font for the content of the thesis by redefining the commands `\rmdefault` and `\sfdefault` as commented out in `these-dbl.cls`.
Currently the latex default font is the one used for the content.


-----
-->

# ![(git logo)](https://yousername.gitlab.io/img/logo_git_50x50.png) Contribute

Merge requests are very welcome.

Maintainers: Pierre-Louis Roman.

Contributors: Louiza Yala (original & main developer), Josquin Debaz, Pierre-Louis Roman, Lucas Bourneuf, Corentin Guezenoc, Clément Elbaz, Florian Arrestier, Alexandre Honorat, Antonin Voyez, Pierre Le Barbenchon, Arthur Lecert, Pascal Cotret, Louis Béziaud, Karol Desnos.

Upstream git repository: https://gitlab.com/ed-matisse/latex-template
