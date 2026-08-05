# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this repository is

`awesome-shell` is a curated, community-maintained **[Awesome list](https://github.com/sindresorhus/awesome)**
of command-line frameworks, toolkits, guides, and gizmos. It is a plain
Markdown link directory — there is **no source code, no build system, no
tests, and no application to run**. The entire "product" is the accuracy,
organization, and quality of the links in `README.md` (and its Chinese
translation `README_ZH-CN.md`).

Any task here is almost always one of: adding/removing/editing a list
entry, reorganizing a section, or fixing a broken link/typo — not software
engineering in the usual sense.

## Repository structure

```text
awesome-shell/
├── README.md          # The list itself (English) — the canonical source
├── README_ZH-CN.md     # Chinese translation of README.md (kept in sync manually)
├── CONTRIBUTING.md      # Scope and inclusion/rejection criteria for entries
└── LICENSE              # CC0 1.0 Universal (public domain dedication)
```

## `README.md` layout

`README.md` opens with an ASCII-art banner and an Awesome badge, then a
table-of-contents linking to each `##`/`###` section, followed by the
sections themselves. Current top-level sections (in order):

- Shells
- Command-Line Productivity (with a `### Directory Navigation` subsection)
- Customization
- For Developers
- System Utilities
- Downloading and Serving
- Multimedia and File Formats
- Applications
- Games
- Shell Package Management
- Shell Script Development
- Guides
- Other Awesome Lists (with a `### See also` subsection)

Each entry is a single Markdown bullet in the form:

```markdown
* [name](https://project-url) - Short, factual description of what it does.
```

Reference-style links (e.g. `[awesome-badge]`, `[awesome-zsh]`) are defined
at the very bottom of the file — follow that pattern for repeated/badge
links rather than inlining the URL again.

If a section has an italicized one-line description under its heading
(e.g. `*Choose your base shell.*` under `## Shells`), preserve that style
when adding new sections.

## Adding or editing entries — follow `CONTRIBUTING.md`

Read `CONTRIBUTING.md` before adding anything. The rules that matter most:

- **Scope:** CLI apps (any language), shell extensions/plugins, and shell
  guides/tutorials are in scope. Shell-specific plugins (e.g. Oh-My-Zsh
  plugins) belong in the dedicated shell's own awesome list
  (`awesome-zsh`, `awesome-fish`, `awesome-bash`), not here, unless
  they're shell-agnostic.
- **Rejected category:** Terminal emulators (iTerm2, Hyper, etc.) do not
  belong here — point contributors to `terminals-are-sexy` instead.
- **Notability bar:** GitHub projects need **at least 50 stars** to be
  eligible, whether self-submitted or submitted by someone else.
  Self-promotion of your own project/guide is explicitly allowed.
- Entries should be placed in the most fitting existing section; only
  introduce a new section/subsection if nothing existing fits and the
  addition doesn't clearly belong in one of the sibling `awesome-*` lists.
- Keep alphabetical ordering within a section/subsection where the
  existing list is alphabetized (most sections are) — check surrounding
  entries and insert in the right place rather than appending at the end.

## Working conventions

- Every change to the English list should be mirrored in
  `README_ZH-CN.md` when practical, or at minimum should not be assumed
  to auto-sync — it's maintained by hand and can lag behind `README.md`.
- Verify links resolve and descriptions are accurate/neutral in tone
  before adding an entry; don't invent star counts or claims about a
  project.
- There is no CI, linter, or test suite — the only "check" is manual
  review against `CONTRIBUTING.md`'s scope and notability rules.
- License is CC0 1.0 (public domain) — no attribution headers or license
  boilerplate needs to be added to content contributions.
- Keep the table of contents at the top of `README.md` in sync with
  actual `##` section headings if you add, rename, or remove a
  top-level section.
