# Commit and Versioning Workflow

Version: 0.1.0
Status: Draft
Style Guide: style-guide--technical-documentation-for-technologists-v0.2.0

## Abstract

This document describes the commit and versioning workflow for `typora-theme-folio`. It covers branch verification, staging, committing with structured messages, tagging, and pushing to origin. It is intended for the project owner and any contributors.

## Initial Commit

### Verify the branch

Confirm the repository is on `main` before making any commits:

```bash
git status
```

If not on `main`, create and switch to it:

```bash
git checkout -b main
```

Note: `git init -b main` will re-initialise an existing repository and emit the following warning, which can be ignored if the repository already exists:

```text
warning: re-init: ignored --initial-branch=main
Reinitialized existing Git repository in /home/<user>/Documents/areas/development/osat-fluent-hugo/.git/
```

### Stage and review

Stage all files:

```bash
git add .
git status
```

The `git status` output after staging is used directly in the commit message. For the initial commit, the expected output is something like this:

```text
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   VERSION
	new file:   accessibility.html
	new file:   codeblock.css
	new file:   credit.html
	new file:   folio-mockup-v0-1-0.html
	new file:   folio-mockup-v0-1-1.html
	new file:   folio-mockup-v0-1-2.html
	new file:   folio-mockup-v0-1-3.html
	new file:   folio.css
	new file:   fonts/cinzel-latin-400-normal.woff2
	new file:   fonts/cinzel-latin-600-normal.woff2
	new file:   fonts/cinzel-latin-ext-400-normal.woff2
	new file:   fonts/cinzel-latin-ext-600-normal.woff2
	new file:   fonts/eb-garamond-latin-400-italic.woff2
	new file:   fonts/eb-garamond-latin-400-normal.woff2
	new file:   fonts/eb-garamond-latin-500-italic.woff2
	new file:   fonts/eb-garamond-latin-500-normal.woff2
	new file:   fonts/eb-garamond-latin-ext-400-italic.woff2
	new file:   fonts/eb-garamond-latin-ext-400-normal.woff2
	new file:   fonts/eb-garamond-latin-ext-500-italic.woff2
	new file:   fonts/eb-garamond-latin-ext-500-normal.woff2
	new file:   mermaid.css
	new file:   sourcemode.css
	new file:   specimen.md

```

### Commit

The commit message opens with a summary line, followed by the staged file list taken directly from `git status` command above. This makes the commit message self-describing without requiring the author to paraphrase what changed.

```bash
git commit -m "Initial commit — v0.1.0
	new file:   VERSION
	new file:   accessibility.html
	new file:   codeblock.css
	new file:   credit.html
	new file:   folio-mockup-v0-1-0.html
	new file:   folio-mockup-v0-1-1.html
	new file:   folio-mockup-v0-1-2.html
	new file:   folio-mockup-v0-1-3.html
	new file:   folio.css
	new file:   fonts/cinzel-latin-400-normal.woff2
	new file:   fonts/cinzel-latin-600-normal.woff2
	new file:   fonts/cinzel-latin-ext-400-normal.woff2
	new file:   fonts/cinzel-latin-ext-600-normal.woff2
	new file:   fonts/eb-garamond-latin-400-italic.woff2
	new file:   fonts/eb-garamond-latin-400-normal.woff2
	new file:   fonts/eb-garamond-latin-500-italic.woff2
	new file:   fonts/eb-garamond-latin-500-normal.woff2
	new file:   fonts/eb-garamond-latin-ext-400-italic.woff2
	new file:   fonts/eb-garamond-latin-ext-400-normal.woff2
	new file:   fonts/eb-garamond-latin-ext-500-italic.woff2
	new file:   fonts/eb-garamond-latin-ext-500-normal.woff2
	new file:   mermaid.css
	new file:   sourcemode.css
	new file:   specimen.md"
```

## Subsequent Commits (With version bump)

For subsequent commits the summary line describes the change and references the new version, and the file list reflects whatever `git status` shows for that commit:

### Commit with version bump

```bash
git commit -m "Bumping version to v0.1.1
	modified:   VERSION
	modified:   en/README.md
"
```

### Tag and push

Apply the version tag, then push both the branch and the tag:

```bash
git tag v0.1.0
git push origin main
git push origin v0.1.0
```

## Subsequent version bumps

**Important Notes**:

* This repository does not make use of language directories at this time
* `bump-version.py` is not included as part of this repository at this time

### bump-version.py process

Use `bump-version.py` to update `VERSION` and `en/README.md`, stage both files, and print the git commands to complete the release:

```bash
python3 bump-version.py 0.1.1 Draft "Brief description of change"
git diff --staged
git commit -m "Bump version to v0.1.1
	modified:   VERSION
	modified:   en/README.md
"
git tag v0.1.1
git push origin main
git push origin v0.1.1
```

## Additional Notes

Once these processes are stable, agreed upon and considered complete this will be promoted to governance

## Changelog

| Version | Status | Notes |
|---------|--------|-------|
| 0.1.0 | Draft | Initial draft |

