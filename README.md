# curriculum-vitae

This repository contains the curriculum vitae (CV) of me, [Gregory M.
Kapfhammer](http://www.cs.allegheny.edu/sites/gkapfham). This repository uses
[gkapfham/research-bibliography](https://github.com/gkapfham/research-bibliography) as a Git submodule to create several
pages of the document in an automated fashion. Parts of this CV are inspired by the example provided at
[moutonf/CV](https://github.com/moutonf/CV), which uses revised versions of the
[moderncv](https://www.ctan.org/pkg/moderncv) and [moderntimeline](https://github.com/raphink/moderntimeline) packages.
As this document is my own customized professional portfolio, I ask that, if you use it as inspiration or for reference,
you suitably customize it for your own purposes. Whenever possible, I would appreciate it if you mention that you used
my CV as a template when creating your document.

### Programming Environment

The curriculum vitae is compiled on an Ubuntu 14.04 LTS workstation using `pdflatex` and
`biber`. You may also compile the paper to a PDF file using a wide variety of other tools, such as `latexmk`. You may
view the resulting PDF file for my CV by visiting my [web site](http://www.cs.allegheny.edu/sites/gkapfham) and
downloading it from the main page. If you are unable to compile create the CV with your development tools and your
execution environment, then please open a new issue and I will attempt to resolve your concerns.

### Creating the Curriculum Vitae

```shell
git clone https://github.com/gkapfham/curriculum-vitae.git
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






