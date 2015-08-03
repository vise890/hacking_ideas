# A better wikipedia #

## The problem: WikiMedia is broken ##

Wikipedia is great. But it's complex markup and platform make contributions
unaccessible to non geeks. This has lead to some subjects (Art history, Design,
Human Geography, etc.) to be grossly underrepresented when compared to STEM
ones.

Also, the fact that content is moderated by the STEM geeks makes becoming a
contributor really hard (you have to learn the markup perfectly, cite
correctly, etcetera). Many changes end up being rejected because of menial
formatting/lack of citations problems. It is an all or nothing thing and people
get discouraged.

Citations are duplicated all over the place. If you want to cite work X 5
times, you gotta duplicate all the info 5 times.

The current wikipedia API is utter crap. It only returns the article's useless
wikiMedia full text and little else.

## Possible Solution ##

An article is just a yaml/toml/json frontmatter and markdonw text. Check the
example below:

```
title: Toilet paper orientation
categories: toilet paper, social psychology, symmetry

---

Toilet paper orientation is a controversial issue blah blah

## History ##
bla bla
```

Use git to manage versions, history, who did what, etc. Use a
fork/modify/create-pull-request to contribute. Pull requests can be commented
on, improved and changed before merging.

This should make it easier for people to contribute to wikipedia.
Search/analysis/data mining should also become trivial (most metadata is
contained in YAML frontmatter, which is easily parsed).

This would make for a nice ass API as well to be easily built.
