# .github

Org-wide defaults for Sprout AI Studio.

## ⚠️ This repository is public

It has to be. GitHub only serves default community health files to private
repositories from a **public** `.github` repo. Every file here is visible to anyone.

Before adding anything, assume it will be read outside the company. No customer names,
no architecture detail, no roadmap, no internal URLs, no credentials. If you wouldn't
put it in a conference talk, it doesn't go here.

## What's in here

| Path | What it does |
|---|---|
| `.github/ISSUE_TEMPLATE/` | The four issue templates. Every repo in the org that has no templates of its own gets these in its "New issue" picker. |
| `.github/ISSUE_TEMPLATE/config.yml` | Turns off blank issues and links the conventions from the picker screen. |
| `CONTRIBUTING.md` | The dictionary — what goes in each section of a ticket. |

## How the inheritance works

A repo with its own file of a given type uses that file. A repo without one falls back
to what's here. Defaults don't appear in any repo's file tree, git history, clones, or
downloads — they're served by GitHub at display time only.

That means editing a template here changes it everywhere at once, and a repo that wants
to opt out just adds its own.

## Changing a template

Open a PR. The ticket process gets reviewed like code.
