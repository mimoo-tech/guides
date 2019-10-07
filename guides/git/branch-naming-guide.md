# Mimoo's Commit Message Guideline

- Start Date: 2019-09-16
- Version: 0.1.0-DRAFT

## Summary

The following guide is a lightweight convention on top of branch naming. It help developers to drive in a standardized way.

## Table of Contents

- [Overview](#overview)
- [Branch Types](#branch-types)
- [Issue Number](#issue-number)
- [Branch Title](#branch-title)
- [Examples](#examples)

## Vocabulary

The wording of each guideline indicates the strength of the rule and the key world "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY" AND "OPTIONAL" in this document are to be interpreted as described in [RF 2119](https://www.ietf.org/rfc/rfc2119.txt).

## Overview

The branch name SHOULD be structure as follows:

```
<type>/<issue-number>/<title>
```

1. A new `branch` SHOULD be create to a specific thing.
2. A new `branch` SHOULD be created for each story.
3. The `branch name` SHOULD always be lowercase as shown below.
4. The `branch name` SHOULD follow the following pattern: type, slash, task number, slash, and finally a title, e.g., `chore/123/git-guidelines`.

## Branch Types

The branch name SHOULD be prefixed with one the following `type`:

```
master: main branch
feat: a feature branch
improvement: a code change that neither fixes a bug nor adds a feature etc
bugfix: a bugfix branch (an bug crops up in development)
hotfix: a hotfix branch (an urgent bug crops up in production)
chore: tool changes, config changes, and changes to things that do not actually go into production at all
```

## Issue Number

1. The `issue number` MUST be an identifier from our correspondent ticket in the Project Management Software.

## Branch Title

1. The `title` MUST be short and descriptive - contain sufficient detail as to the purpose of that branch.
2. The names are separated by hyphens to make the words look easily distinctive as these are often used in URLs.

## Examples

<!-- TODO -->