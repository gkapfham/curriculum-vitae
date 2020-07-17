![build](https://github.com/gkapfham/curriculum-vitae/workflows/build/badge.svg) ![release](https://github.com/gkapfham/curriculum-vitae/workflows/release/badge.svg)

# curriculum-vitae

This repository contains the curriculum vitae (CV) of me, [Gregory M.
Kapfhammer](https://www.gregorykapfhammer.com/). This repository uses
[gkapfham/research-bibliography](https://github.com/gkapfham/research-bibliography)
as a Git submodule to create several pages of the document in an automated
fashion. Parts of this CV are inspired by the example provided at
[moutonf/CV](https://github.com/moutonf/CV), which uses revised versions of the
[moderncv](https://www.ctan.org/pkg/moderncv) and
[moderntimeline](https://github.com/raphink/moderntimeline) packages. As this
document is my own customized professional portfolio, I ask that, if you use it
as inspiration or for reference, you suitably customize it for your own
purposes. If you find this example useful, I would appreciate it if, in addition
to starring the repository, you mention that you used my CV as a template when
creating your document.

## Development Environment

The curriculum vitae is compiled on an Ubuntu 16.04 LTS workstation using
`pdflatex` and `biber`. You may also compile the CV to a PDF file using a wide
variety of other tools, such as `latexmk`. If you are unable to compile the CV
with your development tools and your execution environment, then please open a
new issue and I will attempt to resolve your concerns.

## Creating the Curriculum Vitae

For, clone the repository to your local computer:

```shell
git clone https://github.com/gkapfham/curriculum-vitae.git
```

Now, change into the directory that contains the repository's files:

```shell
cd curriculum-vitae
cd bibliography
git submodule init
git submodule update
cd ../
pdflatex curriculum-vitae-kapfhammer.tex
biber curriculum-vitae-kapfhammer.bcf
pdflatex curriculum_vitae_kapfhammer.tex
pdflatex curriculum_vitae_kapfhammer.tex
```

Before you compile the CV, make sure that you have the bibliography in a Git
submodule:

```shell
cd bibliography
git submodule init
git submodule update
cd ../
```

At this point, you can compile the CV using the following commands:

```shell
pdflatex curriculum-vitae-kapfhammer.tex
biber curriculum-vitae-kapfhammer.bcf
pdflatex curriculum_vitae_kapfhammer.tex
pdflatex curriculum_vitae_kapfhammer.tex
```

Alternatively, you can compile the CV using a single command:

```shell
latexmk -pdf -pvc curriculum_vitae_kapfhammer.tex
```

## Releasing a New Version of the Curriculum Vitae

See what tag you are current on for the repository:

```shell
git describe --tags
```

Set a new tag for the release of the document:

```shell
git tag v1.0.0
```

Note that I follow the [Semantic Versioning Standard](https://semver.org/) when
defining the tags for the release of the curriculum vitae.

Push all of the changes and the new tag to GitHub:

```shell
git push -u origin master --tags
```

New releases of the curriculum vitae are now available through the
[releases](https://github.com/gkapfham/curriculum-vitae/releases) section of the
repository.
