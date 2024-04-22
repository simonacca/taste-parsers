# Taste parsers

Building the wasm parsers from source is a pain because:

- the dependencies are heavy (almost 1GB)
- the dependencies (that is, the individual `tree-sitter-<language>` packages) require a random pile of tools in the environment at `npm install` time
- the dependencies require even more tools at build time

With that in mind, this package vendorizes the parsers (by saving the build output to version control) to ensure a smoother development experience and faster builds.
Nonetheless, this package contains all that is needed to rebuild the parsers from scratch.