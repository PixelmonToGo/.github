# Contributing Guidelines

Contributions are welcome via GitHub pull requests. This document outlines the process to help get your contribution accepted.

Any type of contribution is welcome; from new features, bug fixes, [tests](#testing), documentation improvements

## How to Contribute

1. Fork this repository, develop, and test your changes.
2. Submit a pull request.

***NOTE:*** To make the Pull Requests' (PRs) testing and merging process easier, please submit changes to multiple charts in separate PRs.

### Technical Requirements

* Must pass CI jobs for linting
* Code must be signed off / checked by at least 2 other developers.
* All Technical Changes to Infrastructure **must** be signed off by at least of the Engineers

### Immutability

Any changes to a Mod warrants a version bump even if it is only change to the documentation.

### Versioning

All changes should follow [semver](https://semver.org/).

Any breaking (backwards incompatible) changes should Increase/Bump the MAJOR version. Breaking changes should also include documentation with all relevant and necessary steps for the upgrade.

### Pre-commit

This repo supports the [pre-commit](https://pre-commit.com) framework. By installing the framework (see [docs](https://pre-commit.com/#install)) it is possible to perform the chart linting step before committing your code. This can help prevent linter issues in the pipeline. Note that this requires having Docker running on your development environment.

### PR Approval and Release Process

1. Changes are manually reviewed by PixelMonToGo team members.
1. When the PR passes all tests, the PR is merged by the reviewer(s) in the GitHub `master` branch.
1. Then our CI/CD system is going to generate the relevant release files as required for the changes that have been made.

***NOTE***: Please note that, in terms of time, there maybe a delay of reviewing any PRs. All PRs are reviewed in the order of creation and on a case by case bases.
