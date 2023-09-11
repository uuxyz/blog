---
title: latex usage
date: 2022-04-04
---
Proficient use of LaTeX can help make your research papers appear more standardized and aesthetically pleasing.

First, let's install LaTeX; you can do this by using TeXLive. On a Manjaro system, you can easily install it with the following command:

```bash
sudo pacman -S texlive
```

After completing the installation, it's advisable to create a Git repository for better document management.

Before you begin writing your paper, it's best to use a template from a professional organization like IEEE. Let's create a file named `hello.tex` to start our LaTeX journey. In this file, include the following content:

```latex
\documentclass{IEEEtran}
\title{Hello, \LaTeX}
\author{Your Name}
\begin{document}
\maketitle
\section{Introduction}
This is a simple document.
\section{Hello, World!}
Hello, \LaTeX!
\section{Conclusion}
That's all!
\end{document}
```

Next, compile this `.tex` file using the command line:

```bash
xelatex hello.tex
```

You will then see the resulting PDF file.

If you wish to cite references, you can do so as follows:

Obtain or create a `.bib` file that should look like this:

```bibtex
@article{Einstein1905,
  author = {Albert Einstein},
  title = {On the Electrodynamics of Moving Bodies},
  journal = {Annalen der Physik},
  volume = {17},
  number = {10},
  pages = {891-921},
  year = {1905},
  publisher = {Wiley-VCH}
}
```

Then, add the reference style and citation location to your `.tex` file:

```latex
\documentclass{IEEEtran}
\title{Hello, IEEEtran}
\author{Your Name}
\bibliographystyle{IEEEtran}
\begin{document}
\maketitle
\section{Introduction}
This is a simple IEEEtran document. \cite{Einstein1905}
\section{Hello, World!}
Hello, \LaTeX!
\section{Conclusion}
That's all!
\bibliography{yourbibfile.bib}
\end{document}
```

You can then initialize the references and compile the document using the command line:

```bash
bibtex hello_world.tex
xelatex hello_world.tex
```

This will give you a properly formatted document with citations in IEEEtran style.

Sometimes, changes to references and other content may not get fully updated with a single compilation, requiring us to repeatedly use `xelatex` and `bibtex` for compilation. Alternatively, we can simplify this process by using `latexmk`:

Create a configuration file named `.latexmkrc` if it doesn't already exist. In this file, specify compilation options. Here's an example content for a `.latexmkrc` file:

```bash
$pdflatex = 'xelatex %O -interaction=nonstopmode %S';
$bibtex   = 'bibtex %O %B';
$makeindex = 'makeindex %O -o %D %S';
```

These settings instruct `latexmk` to use `xelatex` for compilation and automatically run `bibtex` and `makeindex` to handle citations and indexes.

Open your command line, navigate to your LaTeX project directory, and run the `latexmk` command:

```bash
latexmk -xelatex your-document.tex
```

Replace `your-document.tex` with the filename of your LaTeX document. The `-xelatex` flag tells `latexmk` to use `xelatex` for compilation.

`latexmk` will automatically detect changes in your document, references, and citations, and run `xelatex`, `bibtex`, and other necessary commands as needed to ensure the final PDF document is generated correctly.

Using `latexmk` or similar build tools can greatly simplify the compilation process of LaTeX documents, eliminating the need to manually run commands multiple times to ensure all changes are properly processed.