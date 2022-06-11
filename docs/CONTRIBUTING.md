# Contributing to PixelmonToGo

✨ Thanks for contributing to **PixelmonToGo**! ✨

As a contributor, here are the guidelines we would like you to follow:
- [How can I contribute?](#how-can-i-contribute)
- [Using the issue tracker](#using-the-issue-tracker)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Coding rules](#coding-rules)
- [Working with our repositories](#working-with-our-repositories)

We also recommend that you read [How to Contribute to Open Source](https://opensource.guide/how-to-contribute).

## How can I contribute?

### Improve documentation

As a **PixelmonToGo** user, you are the perfect candidate to help us improve our documentation: typo corrections, clarifications, more examples, etc.

Please follow the [Documentation guidelines](#documentation).

### Give feedback on issues

Some issues are created without information requested in the [Bug report guideline](#bug-report).
Help make them easier to resolve by adding any relevant information.

Participating in the discussion is a good opportunity to get involved and influence the future direction of **PixelmonToGo**.

## Using the issue tracker

The issue tracker is the channel for [bug reports](#bug-report), [features requests](#feature-request) and [submitting pull requests](#submitting-a-pull-request) only.

Before opening an Issue or a Pull Request, please use the [GitHub issue search](https://github.com/issues?utf8=%E2%9C%93&q=user%3Apixelmontogo) to make sure the bug or feature request hasn't been already reported or fixed.

### Bug report

A good bug report shouldn't leave others needing to chase you for more information.
Please try to be as detailed as possible in your report.

### Feature request

Feature requests are welcome, but take a moment to find out whether your idea fits with the scope and aims of the project.
It's up to you to make a strong case to convince the project's developers of the merits of this feature.
Please provide as much detail and context as possible.

## Submitting a Pull Request

Good pull requests, whether patches, improvements, or new features, are a fantastic help.
They should remain focused in scope and avoid containing unrelated commits.

**Please ask first** before embarking on any significant pull requests (e.g. implementing features, refactoring code), otherwise you risk spending a lot of time working on something that the project's maintainers might not want to merge into the project.

If you have never created a pull request before, welcome 🎉 😄.
[Here is a great tutorial](https://opensource.guide/how-to-contribute/#opening-a-pull-request) on how to send one :)

**Tips**:
- For ambitious tasks, open a Pull Request as soon as possible with the `[WIP]` prefix in the title, in order to get feedback and help from the community.
- [Allow PixelmonToGo maintainers to make changes to your Pull Request branch](https://help.github.com/articles/allowing-changes-to-a-pull-request-branch-created-from-a-fork).
  This way, we can rebase it and make some minor changes if necessary.
  All changes we make will be done in new commit, and we'll ask for your approval before merging them.

## Coding rules

### Source code

To ensure consistency and quality throughout the source code, all code modifications must have:
- No [linting](#lint) errors
- [Valid commit message(s)](#commit-message-guidelines)
- Documentation for new features
- Updated documentation for modified features

### Documentation

To ensure consistency and quality, all documentation modifications must:
- Refer to brand in [bold](https://help.github.com/articles/basic-writing-and-formatting-syntax/#styling-text) with proper capitalization, i.e. **GitHub**, **PixelmonToGo**
- Prefer [tables](https://help.github.com/articles/organizing-information-with-tables) over [lists](https://help.github.com/articles/basic-writing-and-formatting-syntax/#lists) when listing key values, i.e. List of options with their description
- Use [links](https://help.github.com/articles/basic-writing-and-formatting-syntax/#links) when you are referring to:
  - a **PixelmonToGo** concept described somewhere else in the documentation, i.e. How to [contribute](CONTRIBUTING.md)
  - a third-party product/brand/service, i.e. Integrate with [GitHub](https://github.com)
  - an external concept or feature, i.e. Create a [GitHub release](https://help.github.com/articles/creating-releases)
- Use the [single backtick `code` quoting](https://help.github.com/articles/basic-writing-and-formatting-syntax/#quoting-code) for:
  - commands inside sentences, i.e. the `flux` command
  - programming language keywords, i.e. `function`, `async`, `String`
- Use the [triple backtick `code` formatting](https://help.github.com/articles/creating-and-highlighting-code-blocks) for:
  - code examples
  - configuration examples
  - sequence of command lines

### Commit message guidelines

#### Atomic commits

If possible, make [atomic commits](https://en.wikipedia.org/wiki/Atomic_commit), which means:
- a commit should contain exactly one self-contained functional change
- a functional change should be contained in exactly one commit
- a commit should not create an inconsistent state (such as test errors, linting errors, partial fix, feature without documentation, etc.)

A complex feature can be broken down into multiple commits as long as each one maintains a consistent state and consists of a self-contained change.

#### Commit message format

Follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#specification) specification when writing commit messages.


**In summary:**
Each commit message consists of a **header**, and optionally a **body** & a **footer**.
The mandatory header has a special format that includes a **type**, a **subject**, and an optional **scope**:

```commit
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

An exclamation mark (!) must be added after the scope to indicate a **BREAKING CHANGE**.

The **footer** can contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages).

#### Type

The type must be one of the following:

| Type         | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| **chore**    | Any non-functional changes (i.e. documentation CI config, formatting, and external dependencies)            |
| **feat**     | A new feature                                                                                               |
| **fix**      | Any change, patch, or bugfix to an existing feature                                                         |

#### Subject

The subject contains succinct description of the change, to be clearly understood by a quick observation:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize letters where possible
- no dot (.) at the end

#### Body
Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior if more detailed explanation is required.

#### Footer
The footer should contain any information about **Breaking Changes** and is also the place to reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.
The rest of the commit message is then used for this.

#### Examples

```commit
fix(pencil): stop graphite breaking when too much pressure applied
```

```commit
feat(pencil): add 'graphiteWidth' option

Fix #42
```

```commit
feat(pencil)!: remove graphiteWidth option

BREAKING CHANGE: The graphiteWidth option has been removed.

The default graphite width of 10mm is always used for performance reasons.
```

## Working with our repositories

### Lint

All [PixelmonToGo](https://github.com/PixelmonToGo) repositories use [MegaLinter](https://megalinter.github.io/latest/) for linting and formatting, alongside [pre-commit](https://pre-commit.com/) for validation.

### Versioning

We follow [semver](https://semver.org/) when versioning our artifacts, this should be automated as a result of following the [commit message format](#commit-message-format) using [release-please](https://github.com/googleapis/release-please) where possible.

### Pre-commit

Installing [pre-commit](https://pre-commit.com/) (see [docs](https://pre-commit.com/#install)) will allow you to validate your change before committing. This can help prevent linter issues in the pipeline and save some time during the Pull Request review process.

### Merging and releasing

- Changes by humans are always manually reviewed in the order they are submitted by [PullRequest](https://www.pullrequest.com/) and [PixelmonToGo](https://github.com/orgs/PixelmonToGo/people) team members.
- If your Pull Request complies with the contributing standards in this document, and the change is accepted, it will be merged.
- Release pipelines should automatically generate the relevant artifacts following a successful merge to a repository's `main` branch.
