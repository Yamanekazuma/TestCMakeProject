# TestCMakeProject
[![MSBuild](https://github.com/Yamanekazuma/TestCMakeProject/actions/workflows/msbuild.yml/badge.svg?branch=main)](https://github.com/Yamanekazuma/TestCMakeProject/actions/workflows/msbuild.yml)

Practice for CI/CD.

## On create/edit Pull Request
1. Auto refactor with clang-format.
2. Analyze with lizard.
3. Build all variants.

## Release flow
- `major`/`minor` label causes major/minor update.
- PRs from a particular label/branch name will be appended to the corresponding section of the release notes.
- Version update/release creation is done by manually invoking the Release action.
