# GithubActions
This repo is for learn about git hub actions
EX
on: push
jobs:
  test:
    strategy:
      matrix:
        platform: [ubuntu-latest, macos-latest, windows-latest]
    runs-on: ${{ matrix.platform }}
    steps:
    - uses: actions/checkout@v1
    - uses: actions/setup-node@v1
      with:
        version: 12
    - run: npm install-ci-test
    - uses:
