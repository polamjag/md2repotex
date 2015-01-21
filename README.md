# md2repotex

Markdown to LaTeX converter, wraps pandoc, appends header and footer

## DEPENDENCIES

- [Pandoc](http://johnmacfarlane.net/pandoc/)
- GNU sed

## SYNOPSIS

```
$ md2repotex [-t ""] [-d "\\today"] [-f] <source markdown file> # generates .tex file here
```

### OPTIONS

- `-t ""`: title for report
- `-d "\\today"`: specify `\date{}` in LaTeX (the character `\\` should be doubled because it works as escape sequence)
- `-f`: force overwriting output file

## DESCRIPTION

**You must have directory named `.md2repotex.d/` in your `$HOME`**.

Edit thees files to customize template for generated files.

It contains these files:

  - `.md2repotex.d/meta`
  - `.md2repotex.d/header`
  - `.md2repotex.d/footer`

### `.md2repotex.d/meta`

This file contains metadata of the document like `\author`.

### `.md2repotex.d/header`

This file contains basic preambles for LaTeX files.

### `.md2repotex.d/footer`

This file is basically only for `\end{document}`, but you can append anything on bottom of .tex file by editing this.
