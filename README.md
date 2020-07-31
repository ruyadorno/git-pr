# git-pr

[![NPM version](https://img.shields.io/npm/v/@ruyadorno/git-pr)](https://www.npmjs.com/package/@ruyadorno/git-pr)
[![License](https://img.shields.io/github/license/ruyadorno/git-pr)](https://github.com/ruyadorno/git-pr/blob/master/LICENSE)
[![Join the chat at https://gitter.im/ipipeto/Lobby](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/ipipeto/Lobby)

Git plugin that allows you to interactively list open PRs from a GitHub repo and checkout a selected PR... AND MORE!

> An [iPipeTo](https://github.com/ruyadorno/ipt) workflow

<br />
<br />

<p align="center">
<img alt="demo animation" width="600" src="https://ruyadorno.github.io/svg-demos/git-pr/demo.svg" />
</a>
</p>

<br />

## Install

Get it with **npm**:

```sh
npm install -g @ruyadorno/git-pr ipt json
```

\*Also needs the [GitHub cli installed in your system](https://github.com/cli/cli#installation)

### Run

In any git repo folder to list currently open PRs and checkout:

```
git pr
```

**OR**

bypass **npm install** and run it at once using **npx**:

```sh
npx @ruyadorno/git-pr
```

## Features

- Interactively listing all current open PRs on Github and:
  - Checking out from that branch
  - Showing the diff for files
  - Closing, Merging (and reopening) a PR
  - Reviewing a PR
  - View description for that open PR
- Listing PRs open in GitHub from you current repo

## Requirements

- [GitHub cli](https://github.com/cli/cli#installation)
- `json` [npm i -g json](https://www.npmjs.com/package/json)
- `ipt` [npm i -g ipt](https://www.npmjs.com/package/ipt)

## Help

```
Usage:
    git pr
    git pr [<cmd>]

Commands:
git pr              Checkout from an interactive list of all open PRs
git pr clean        Cleans up after checking out a branch from a fork
git pr close        Closes the PR selected from the interactive list
git pr diff         See diff for the selected PR from an interactive list
git pr help         Shows this help message
git pr list         Only lists the current open PRs
git pr merge        Merges the selected PR
git pr push         Push commits to the branch of prev selected PR
git pr reopen       Reopens the selected closed PR
git pr review       Review the selected PR from the cli
git pr status       Status of all open PRs
git pr version      Shows current version number
git pr view         See info for the selected PR

Requirements:
This tool requires the following cli to be available in your system:
- GitHub cli (https://github.com/cli/cli#installation)
- json [npm i -g json](https://www.npmjs.com/package/json)
- ipt [npm i -g ipt](https://www.npmjs.com/package/ipt)
```

### Equivalent bash alias

Although less powerful, this bash alias achieves roughly the same base usage of listing and checking out a single PR (it still requires `ipt` or equivalent and `gh` to be installed in your system).

```sh
alias git-pr="gh pr list | ipt -u | cut -f 3 -d $'\t' | xargs gh pr checkout"
```

## License

[MIT](LICENSE) © 2020 [Ruy Adorno](https://ruyadorno.com)
