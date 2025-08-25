## How to build myst site and paper


This site is build with [mystmd](https://mystmd.org/guide)


To build the site, from command line type:
`myst start`

- This will typically open a working local version of the site at http://localhost:3000/
- With github actions we can set this up to trigger a build of a site on github pages.

Necessary files: 

myst.yml  - configuration file
_toc.yml  - table of contents

Additionally myst markdown and directives in jupyter notebooks and markdown files.  Yaml at the front of files selects templates and other options.


To build the PDF version of the paper:
```bash
myst build docs/crime_paper.md --pdf
```
