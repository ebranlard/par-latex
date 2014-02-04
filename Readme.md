# par-latex

A quick and dirty script to reformat latex paragraphs or entire latex documents. The script reads from standard input (or 1st argument) and writes to standard output. 

It is written in python, intended to be used with Vim but is not restricted to it.

## Parameters / functionalities
Parameters at the beginning of the scripts determine:
- `width`: the paragraph width.
- `latex_command_count`: whether latex commands such as \ref or \cite should be reformatted or if the reformatting stop when they are encountered. (Default True)
- `format_inside_group`: whether formating is done between "begin" and "end" groups. (Default False)

Functionalities:
- Sections titles are not reformatted.
- The presence of a comment stops the formatting of the current paragraph, the formatting will start again at the next line.





## Installation
Put the script `par-latex` in your path and make it executabe with `chmod +x par-latex` (for linux)


## Example from command line
```
    cat file.tex|par-latex
```
```
    par-latex file.tex
```

## Example of usage in vim
- Select some text (e.g.  `Vj` or `ggVG`)
- type ":!par-latex"  (vim command line looks like: `'<,'>!par-latex`)
- type enter

