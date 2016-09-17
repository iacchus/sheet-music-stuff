# The ABC Music Notation Standard 2.1 (Dec 2011)

Here, I used [pandoc](pandoc.org) to render the [abc music notation standard](http://abcnotation.com/wiki/abc:standard:v2.1) to various formats.

## The Files

| Format           | File link                            | Command to generate file |
| ---------------- | ------------------------------------ | -------------------------|
| GitHub Markdown  | [abcnotation.md](abcnotation.md)     | `pandoc abcspec.html -t markdown_github -o abcnotation.md` |
| HTML             | [abcnotation.html](abcnotation.html) | `pandoc abcspec.html --standalone --self-contained -t html5 -o abcnotation.html` |
| PDF              | [abcnotation.pdf](abcnotation.pdf)   | `pandoc abcnotation.md metadata.yaml -s --latex-engine xelatex -o abcspec.pdf` |
| Plain Text       | [abcnotation.txt](abcnotation.txt)   | `pandoc abcspec.html -t plain -o abcnotation.txt` |
| AsciiDoc         | [abcnotation.adoc](abcnotation.adoc) | `pandoc abcnotation.md -t asciidoc -o abcnotation.adoc; mv abcnotation.adoc abcnotation.bugged.adoc; sed 's/link\:\[\]//g' abcnotation.bugged.adoc > abcnotation.adoc` |


