# CLAUDE.md

Guidance for Claude Code (or any AI assistant) working in this repository.

## What this repository is

`awesome-shell` is a curated, link-only [Awesome List](https://github.com/sindresorhus/awesome) of
command-line frameworks, toolkits, guides, and utilities. There is no source code, no build system,
and no application to run — the entire deliverable is Markdown content in two README files.

## Repository structure

```
.
├── README.md            # The list itself (English) — primary source of truth
├── README_ZH-CN.md       # Simplified-Chinese translation of README.md
├── CONTRIBUTING.md       # Scope and inclusion/rejection criteria for new entries
├── LICENSE               # CC0 (public domain dedication)
└── .github/workflows/ci.yml  # Link-checker CI (lychee)
```

There are no other directories — no `src/`, no package manifests, no tests in the conventional sense.

## Content conventions

`README.md` is organized as a table of contents followed by `##`/`###` sections, each holding an
alphabetized bullet list of entries. Existing top-level sections (keep new entries under the closest
matching one, don't invent new top-level sections without reason):

- Shells
- Command-Line Productivity (with a Directory Navigation subsection)
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
- Other Awesome Lists

Each entry follows this exact format:

```
* [name](https://link) - Short, factual, sentence-fragment description.
```

- Entries within a section are alphabetized (case-insensitive) by name.
- Descriptions are terse, third-person, and end without a trailing period in most existing entries —
  match the surrounding style rather than imposing new punctuation rules.
- The table of contents near the top of `README.md` must stay in sync with the `##` section headers
  (anchors are auto-generated from heading text).
- `README_ZH-CN.md` is a manually maintained translation. It is **not** required to be updated in
  lockstep with every English change — but if you touch major structure (section headers, TOC), check
  whether the Chinese version needs the same structural update. Do not machine-translate wholesale;
  prefer leaving it stale over producing low-quality translation.

## Inclusion criteria (see `CONTRIBUTING.md` for full detail)

When asked to add, vet, or review an entry:

- **Scope**: CLI apps (any language), shell-specific extensions/plugins, and shell scripting
  guides/tutorials are in scope. Terminal emulators (Hyper, iTerm2, etc.) are explicitly **out of
  scope** — redirect those to `terminals-are-sexy`.
- **Shell-specific plugins** (e.g. Oh-My-Zsh plugins) belong in a shell-specific list
  (`awesome-zsh-plugins`, `awesome-fish`, `awesome-bash`), not here, unless they're shell-agnostic.
- **Notability**: GitHub projects need at least 50 stars to be considered. Self-submission of your
  own project is explicitly allowed.
- Sibling "Awesome Zsh/Fish/Bash" lists are linked but not maintained in this repo.

## CI / validation

`.github/workflows/ci.yml` runs on every push to `master` and every PR: it uses
[lychee](https://github.com/lycheeverse/lychee-action) to check that every link in `README.md` and
`README_ZH-CN.md` resolves (with `www.passwordstore.org/*` excluded from checks). There is no other
CI. Before proposing changes that add or edit links, sanity-check the URLs are correct — broken links
will fail CI.

There are no lint/build/test commands to run locally beyond checking Markdown renders correctly and
links are valid.

## Making changes

1. Add/edit entries directly in `README.md`, keeping alphabetical order within the target section.
2. Keep the table of contents accurate if you add/remove/rename a section.
3. Do not add terminal emulators, low-star/unnotable projects, or duplicate entries.
4. Prefer small, focused diffs — one logical change (e.g. one new tool) per commit/PR, consistent with
   the repo's history of incremental single-entry additions.
5. This is a community list with an established, mostly-hands-off maintenance history — avoid
   sweeping reorganizations unless explicitly asked.
