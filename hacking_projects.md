# Ion shell

Clojure wrapper for [Electron](http://electron.atom.io)


# Drug interaction

- crowd-sourced data for drugs
- app warns you of possible negative interactions between drugs


# jiki

Serve a folder of .md files, wiki-style. Support Search. Later, citations (through gocite).


# Pair Reactor

"Dating" website to find remote pairs to work on FOSS projects


# Hmail

REST json wrapper over IMAP, SMPTP and GPG. Sending email is:
```
POST {to: 'bobby@bob.com',
      from: 'vise@viselabs.com',
      subject: 'bla',
      body: 'blabla'}
     /email
```

This looks for and fetches bobby's public key from e.g. `pgp.mit.edu`, encrypts the mail and sends it.

Similarly, getting email is:

```
GET /email
```

and you get:

```
[{to: "", from: "", datetime: "", body: "", ...}]
```


# [scotty](./detailed/scotty.md)

A simple energy simulation engine.


# App for studio di settore

...and sell that shit for much profit


# [gocite](./detailed/gocite.md)

An open, collaborative database for technical citations


# GoTypeset

dockerized LaTeX typesetting server
- POST /typeset {something.md} => something.pdf


# [PaperWare](./detailed/scihub.md)

Write science better. Together (A github for technical writing, books, papers, research, projects..)


# [gojure](./detailed/gojure.md)

Clojure dialect for the golang ecosystem


# [pickpocket](./detailed/pickpocket.md)

Scrape reading list from pocket, put it in sane plain-text format.


# [juicer](./detailed/juicer.md)

HTML content extractor for the CLI.


# [koji](./detailed/koji.md)

Format for building and representing knowledge graphs.


# SOT (Science of Trust)

WOT for publications


# organization software

- notes, thoughts, what this org folder does (or tries to do...)
- full text searchable
- the simplicity of pocket
- taggable, view by tag
  - suggest tags for new content
- quick to add a new fragment to (inbox) (doesn't go away untill is tagged)
- I am starting to suspect that this may be org mode


# [wikimedia-2.0](./detailed/better_wikimedia.md)

jiki + SOT + gocite + git
- need a mediawiki format parser (elixir?)


# [nimble wall](./detailed/nimble_wall.md)

Sanely manage agile walls.

# modium (rust)

Convert in between full and octal UNIX permission representations.


# Puddle

README.md -> splash-page.html


# 'Due' for android/FF OS

- recurring todos
- can postpone them (just for today)
- can dismiss them before they are due


# Add neovim as an atom/emacs backend

# PWUpd8
db of scripts to update password on websites (capybara)
