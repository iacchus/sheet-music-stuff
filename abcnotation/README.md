# The ABC Music Notation Standard 2.1 (Dec 2011)

Here, I used [pandoc](pandoc.org) to render the [abc music notation standard](http://abcnotation.com/wiki/abc:standard:v2.1) to various formats.

## The Files

| Format           | File link                            |
| ---------------- | ------------------------------------ |
| GitHub Markdown  | [abcnotation.md](abcnotation.md)     |
| HTML             | [abcnotation.html](abcnotation.html) |
| PDF              | [abcnotation.pdf](abcnotation.pdf)   |
| Plain Text       | [abcnotation.txt](abcnotation.txt)   |
| AsciiDoc         | [abcnotation.adoc](abcnotation.adoc) |

## The commands used to create them

### GitHub Markdown

`pandoc abcspec.html -t markdown_github -o abcnotation.md`

### HTML5

`pandoc abcspec.html --standalone --self-contained -t html5 -o abcnotation.html`

### PDF 

`pandoc abcspec.html metadata.yaml -s --latex-engine xelatex -o abcspec.pdf`

### Plain Text

`pandoc abcspec.html -t plain -o abcnotation.txt`

### AsciiDoc

`pandoc abcnotation.md -t asciidoc -o abcnotation.adoc`

