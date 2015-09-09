# Pair Reactor

OKCupid for finding the perfect pair and contribute to FLOSS projects.

You give me the language, your proficiency in it, the projects
you want to contribute to, pair reactor gives you matches.


# Hmail

REST json wrapper over IMAP, SMPTP and GPG. Sending (encrypted) email is:
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
[{to: "vise@viselabs.com",
  from: "bla@bla.com",
  datetime: "Stardate 4282",
  subject: "foo",
  body: "Thrusters on full"},
 {...}]
```


# [SciHub](./detailed/scihub.md)

Write science better. Together.
A GitHub for technical writing, books, papers, research, undergraduate engineering group projects..

The best environment to collaborate on technical writing.

Bring the fork/modify/PR/RFC model to science!


# jiki

Transform a folder of markdown files to a full blown, browseable site.

Features:
- Tree view/list view (list files);
- Full text search;
- Citations (through [gocite](./detailed/gocite.md)).

Possible uses:
- Project documentation (keep a `docs` folder in a project root)
- Personal blog
- Any wiki


# [gocite](./detailed/gocite.md)

An open, collaborative database for technical citations


# [Passlord](./detailed/passlord.md)

A pretty unixy password manager.


# `mdfmt`

A markdown formatter/beautifier in the spirit of `gofmt`.


# [scotty](./detailed/scotty.md)

A simple energy simulation engine.


# Sparkel

Tinder for startup finders.

Give your idea, find co-founders.


# Drug interaction

- crowd-sourced data for drugs
- app warns you of possible negative interactions between drugs


# [wikimedia-2.0](./detailed/better_wikimedia.md)

jiki + SOT + [gocite](./detailed/gocite.md) + git


# Ion shell

Clojure wrapper for [Electron](http://electron.atom.io)


# App for studio di settore

...and sell that shit for much profit

[Started in clojure](https://github.com/vise890/studio-settore)


# [GoTypeset](https://github.com/vise890/gotypeset)

dockerized LaTeX typesetting server

`POST /typeset {something.md} => something.pdf`

Integrated with [gocite](./detailed/gocite.md) for citations


# [nimble wall](./detailed/nimble_wall.md)

Sanely manage agile walls.


# [gojure](./detailed/gojure.md)

Clojure dialect for the golang ecosystem.


# [pickpocket](./detailed/pickpocket.md)

Scrape reading list from pocket, put it in sane plain-text format.


# [juicer](./detailed/juicer.md)

HTML content extractor for the CLI.


# [koji](./detailed/koji.md)

Format for building and representing knowledge graphs.


# Puddle

README.md / some JSON -> splash-page.html


# SOT (Science of Trust)

WOT for publications


# modium (rust)

Convert in between full and octal UNIX permission representations.


# 'Due' for android/FF OS

- recurring todos
- can postpone them (just for today)
- can dismiss them before they are due


# Add neovim as an atom/emacs backend


# PWUpd8

db of scripts to update password on websites (capybara)

# organization software

- notes, thoughts, what this org folder does (or tries to do...)
- full text searchable
- the simplicity of pocket
- taggable, view by tag
  - suggest tags for new content
- quick to add a new fragment to (inbox) (doesn't go away untill is tagged)
- I am starting to suspect that this may be org mode
