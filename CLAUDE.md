# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This is a small personal test/sandbox repository (`test`), not a buildable application. It has no package manager, build tool, linter, or test suite configured. Contents are unrelated, standalone artifacts:

- `index.html` — a static Bootstrap 4.5 HTML snippet (loads Bootstrap CSS/JS and jQuery/Popper from CDNs via `<link>`/`<script>` tags). It references `site.webmanifest` and `icon.png`, neither of which exists in the repo. There is no dev server or build step — open the file directly in a browser to view it.
- `test.java` — a standalone `HelloWorld` class. Compile/run directly with `javac test.java && java HelloWorld` (no build tool, no package declaration).
- `test_sorce/` — miscellaneous scratch content (e.g. `aaa.txt`, currently empty).

## Working in this repo

Because there is no shared build/test tooling, treat each file as independent: verify changes by compiling/opening the specific file you touched (e.g. `javac`/`java` for the `.java` file, opening `index.html` in a browser) rather than assuming a repo-wide command exists.
