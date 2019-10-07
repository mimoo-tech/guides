# Mimoo's Commit Message Guideline

- Start Date: 2019-09-13
- Version: 0.1.0-DRAFT

## Summary

Inspired by [Karma's style guide](http://karma-runner.github.io/4.0/dev/git-commit-msg.html) and [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.4/) for Git commit messages, the following guide is a lightweight convention on top of commit messages. It help to clarify the record of change to a project and help focus commits into scoped segments.

## Table of Contents

- [Overview](#overview)
- [Message subject (first line)](#message-subject-first-line)
- [Message body](#message-body)
- [Message footer](#message-footer)
- [Examples](#examples)
    - [Commit message with no body](#commit-message-with-no-body)
    - [Commit message with description and breaking change in body](#commit-message-with-description-and-breaking-change-in-body)
    - [Commit message for a fix using an (optional) issue number](#commit-message-for-a-fix-using-an-optional-issue-number)

## Vocabulary

The wording of each guideline indicates the strength of the rule and the key world "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY" AND "OPTIONAL" in this document are to be interpreted as described in [RF 2119](https://www.ietf.org/rfc/rfc2119.txt).

## Overview

The commit message SHOULD be structure as follows:

```
<type>: <description>

[optional body]

[optional footer]
```

## Message subject (first line)

The commit messages SHOULD be prefixed with one the following `type`:

```
feat: a new feature for endusers
fix: a bugfix for endusers (not a build-process fix)
docs: documentation only changes
style: changes that do not affect the meaning of the code (e.g.: white-space, formatting, missing semi-colons...)
refactor: refactor production code (e.g.: renaming a variable...)
improvement: a code change that neither fixes a bug nor adds a feature etc
perf: a code change that improves performance
test: adding missing tests or correcting existing tests
build: changes that affect the build system or external dependencies (e.g.: gulp, broccoli, npm...)
ci: changes to our ci configuration files and scripts (e.g.: circle, browserstack, saucelabs...)
```

1. The `subject` SHOULD always be lowercase as shown below.
2. Commits MUST be prefixed with a `type`, which consists of a noun, feat, fix, etc., and a REQUIRED terminal colon and space.
2. A `description` MUST immediately follow the space after the `type` prefix. The `description` is a short summary of the code changes, e.g., `docs: add git commit message guide`.
3. A `!` MUST be appended prior to the `:` in the type prefix, to futher draw attention to breaking changes.

## Message body

1. A longer commit `body` MAY be provided after the short description, providing additional contextual information about the code changes. The body MUST begin one blank line after the `description`.
2. A message MUST use the imperative, present tense, e.g., "change" not "changed" nor "changes".
3. Breaking changes MUST be indicated at the very beginning of the body section. A breaking change MUST consist of the uppercase text `BREAKING CHANGE`, followed by a colon and a space.
4. A description MUST be provided after the `BREAKING CHANGE:`, describing what has changed about the API, e.g., `BREAKING CHANGE: environment variables now take precedence over config files`.

## Message footer

1. A `footer` of one or more lines MAY be provided one blank line after the body. The `footer` MUST contain meta-information about the commit, e.g., related pull-requests, closed issues, etc., with one piece of meta-information per-line.

## Examples

### Commit message with no body

```
docs: add git commit message guide
```

### Commit message with description and breaking change in body

```
refactor!: rename array variables to be plural

BREAKING CHANGE: a new version of api was generated (v2) as the change will break the current contract
```

### Commit message for a fix using an (optional) issue number

```
fix: correct an query clause of xpto module

see the issue for details on the fields fixed

closes #1
```