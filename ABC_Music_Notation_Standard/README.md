# The ABC Music Notation Standard 2.1 (Dec 2011)

Here, I used [pandoc](pandoc.org) to render the [abc music notation standard](http://abcnotation.com/wiki/abc:standard:v2.1) to various formats.

## The Files

| Format           | File link                            | Command to generate file |
| ---------------- | ------------------------------------ | -------------------------|
| GitHub Markdown  | [abcnotation.md](abcnotation.md)     | `pandoc abcspec.html -t markdown_github -o abcnotation.md` |
| HTML             | [abcnotation.html](abcnotation.html) | `pandoc abcspec.html --standalone --self-contained -t html5 -o abcnotation.html` |
| PDF              | [abcnotation.pdf](abcnotation.pdf)   | READ BELOW |
| Plain Text       | [abcnotation.txt](abcnotation.txt)   | `pandoc abcspec.html -t plain -o abcnotation.txt` |
| AsciiDoc         | [abcnotation.adoc](abcnotation.adoc) | `pandoc abcspec.html -t asciidoc -o abcnotation.adoc -t asciidoc -o abcnotation.adoc; mv abcnotation.adoc abcnotation.bugged.adoc; sed 's/link\:\[\]//g' abcnotation.bugged.adoc > abcnotation.adoc` |

## Converting to PDF

The PDF version was first converted to LaTeX, then the [latex file](abcnotation.tex) was edited, and `xelatex` was used to generate the pdf.

### 1. Converting to standalone HTML (without embedded images)

`pandoc abcspec.html --standalone -t html5 -o abcnotation_nodata.html`

### 2. Converting to LaTeX (.tex)

`pandoc abcnotation_nodata.html metadata.yaml --standalone -f html -t latex -o abcnotation.tex`

### 3. Making changes to .tex file

Then I made some changes to .tex file, before compiling to PDF.

### 4. Converting to PDF

`xelatex abcnotation.tex`
