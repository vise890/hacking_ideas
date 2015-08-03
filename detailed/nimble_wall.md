# Nimble

Nimble is a CLI command suite that helps you manage an agile wall. It uses markdown files to represent tasks and directories to represent swimming lanes.

Nimble is designed to be simple and extensible:

  - it relies on VCS to track story movement and changes, and to stay in sync with the team.
  - its commands mimic UNIX commands (e.g., mv, ls)


# Getting Started

You can create a new wall with:
```bash
$ nim init  # initializes an empty story wall in `nimble-wall`
```
A story wall is just a directory. It contains a number of other directories that represent swim lanes.
The default swim lanes are:

  - backlog (bl)
  - in_analysys (an)
  - ready_for_dev (rdev)
  - in_dev (dev)
  - ready_for_qua (rqa)
  - in_qua (qa)
  - ready_for_showcase (rshow)
  - ready_for_production (rprod)

The names in brackets are aliases for the full swim lane name.

New swim lanes can be created with:
```bash
$ nim new lane archive      # makes a new swim lane called `archive`
```

Each swim lane contains plain-text files that represent user stories. Most information is contained in the file name.
However, more detail (e.g., acceptance criteria) can be addedd in the file contents.

A new story can be created with:
```bash
$ nim new story user can edit own profile
```

New tasks and defects can be created with:
```bash
$ nim new task fix functional tests in ci environment
$ nim new defect a user can view orders that belong to other users
```

By default, all new stories, tasks and defects start in the backlog.
You can create a story in a new lane with:
```bash
$ nim new task -l dev migrate to phantomjs in functional tests
    # creates a new task in dev (in_dev)
```

```bash
$ nim ls                    # list all the stories
$ nim ls rdev               # list all the stories in rdev (ready for dev)
$ nim ls ready_for_dev      # list all the stories in rdev (ready for dev)
$ nim ls dev                # list all the stories in dev (in_development)

$ nim ls @backend           # list all the stories tagged with `@backend`

$ nim info 123              # displays the long description of story #123
$ nim info -                # displays the long description of the last viewed story

$ nim mv qa/123 showcase    # move story 123 from qa (in_qa) to showcase (ready_for_showcase)
$ nim mv --next 123         # move story 123 to the next swim lane
```

# Frontends
You need them, but the format would make it sane enough to build them on top of it
