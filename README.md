## What

"This is a Github action to prevent the increase of duplicated code. 

If the duplicated code exceeds the threshold, it will issue a warning in the comments on the PR."

![CleanShot 2023-11-29 at 15 18 21](https://github.com/wix-incubator/jscpd-check/assets/24843808/16823328-ce83-44ca-a1df-7452b973ac61)


## Usage

```yml
name: Use Code Duplication Check

on: [pull_request]

permissions:
  issues: write
  pull-requests: write

jobs:
  call-jscpd-check:
    uses: wix-incubator/jscpd-check/.github/workflows/pr-code-duplication-check.yml@master
    with:
      TARGET: "src"
      THRESHOLD: 1
```
