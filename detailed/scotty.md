# Scotty

A simple energy simulation engine.

This is basically an incremental [ESP-r](https://en.wikipedia.org/wiki/ESP-r) rewrite (not in Fortran).

The beginning could be some simple formats (e.g. clojure/JSON data structures) to represent:
- geometry
- constructions
- materials
- operations
- (weather)

.. which are then converted to `.opr`, `.geo`, etc. files that ESP-r can use. i.e.:
Input: geometry, constructions, weather, operations
Output: ESP-r sym

Later, using these sane formats (that don't require thousands of LOC in Fortran to parse and write...) could
be the basis for a full rewrite in Julia or something.

