# Citation db for scientific publishing

Writing in markdown is nice. Citing works in it is not. It is even more awful in
bibtex.

Gocite should really be 2 things:

1. a CLI application
2. a RESTful service

## 1. The CLI

```bash
$ gocite dissertation.tex db.bib
```

1. Scans `dissertation.tex` for `\citep` commands, gets all the citation IDs.
2. Performs the adequate magic (through the RESTful service).
3. Creates a bibtex db in `db.bib`


## 2. the API for citations/refs

Citedb should have a badass and stupidly simple API:

```
GET /sust2011hendley
=> {type: 'book',
    year: 2011,
    author: 'hendley',
    title: 'sustainable building desingn in tropical climates',
    publisher: 'blah words',
    ...}
    
PATCH /book/sust2011hendley

GET /sust2001hendley.bib
=> "
@book{book,
  author    = {Peter Hendley}, 
  title     = {Sustainable building design in tropical climates},
  publisher = {blah words},
  year      = 2011,
  address   = {The address},
  edition   = 3,
  month     = 7,
  ...
}
"
```
