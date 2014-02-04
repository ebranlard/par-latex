## par-latex

A quick and dirty script to reformat latex paragraphs or entire latex documents. The scripts uses reads from standard input (or 1st argument) and writes to standard output. 

It is written in python, intended to be used with Vim but not restricted to it.

# Parmeters
Parameters at the beginning of the scripts determines:
- width:the paragraph width.
- latex_command_count: whether latex commands such as \ref or \cite should be reformatted or if the reformatting stop when they are encountered. (Default True)
- format_inside_group: whether formating is done between "begin" and "end" groups. (Default False)


# Installation
Put the script par-latex in your path.
Make it executabe `chmod +x par-latex`


# Example from command line
```
    cat file.tex|par-latex
```
```
    par-latex file.tex
```

# Example of usage in vim
- Select some text (e.g.  `Vj` or `ggVG`)
- type ":!par-latex"  (vim command line looks like: `'<,'>!par-latex`)
- type enter

