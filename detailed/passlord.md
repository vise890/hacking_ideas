# Passlord

A collection of JSON files in a directory.
  - each is crypted with GPG
  - uses same structure as `pass` (and indeed use [`pass`](http://www.passwordstore.org/))

Open standard for storing passwords as JSON:
(for example)
```json
{
  "username": "foo",
  "password": "megaseek",

  "urls": ["www.foo.com/*", "mail.foo.com/*"],

  "username_css_selectors": ["#username"],
  "password_css_selectors": ["#password"]
}
```

## password manager
- server exposes an API to serve the JSON files
- client (browser ext in cljs)
  - pings the API according to current site
  - asks for password
  - fills forms
