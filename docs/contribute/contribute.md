# How to contribute

There are many ways to contribute to nodecg-io: logging bugs, submitting pull
requests, reporting issues, and creating suggestions. You can also contribute to
this [documentation](docs_setup.md).

First you'll need an installation of nodecg-io. Please refer to the
[installation guide](../getting_started/install.md) and create a development
installation. The CLI asks you whether you want to clone the documentation. It's
highly recommended that you do that and update the documentation as you add new
services or features. To be able to create Pull Requests you should fork the
corresponding repositories and add them as a remote (update URL for e.g.,
documentation repository):

```shell
git remote add fork https://github.com/[YOUR_USERNAME]/nodecg-io.git
```

Then you can create a new branch, do your changes, create commits and publish
the branch to your fork using the following command:

```shell
git push fork my-branch
```

## Build

### VS Code

In Visual Studio Code you can start the build task with <kbd>Ctrl</kbd> +
<kbd>Shift</kbd> + <kbd>B</kbd> (<kbd>CMD</kbd> + <kbd>Shift</kbd> +
<kbd>B</kbd> on macOS). The incremental builder will do an initial full build.  
The watch builder will watch for file changes and compile those changes
incrementally, giving you a fast, iterative coding experience. It will even stay
running in the background if you close VS Code. You can resume it by starting
the build task with <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>B</kbd>
(<kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>B</kbd>) again.  
You can kill the build task by pressing <kbd>Ctrl</kbd> + <kbd>D</kbd> in the
task terminal (<kbd>CMD</kbd> + <kbd>D</kbd>) on macOS.  
Errors and warnings will be shown in the status bar at the bottom left of the
editor. You can view the error list using `View | Errors and Warnings` or
pressing <kbd>Ctrl</kbd> + <kbd>P</kbd> and then <kbd>!</kbd> (or
<kbd>CMD</kbd> + <kbd>P</kbd> and <kbd>!</kbd> on macOS).

### Terminal

You can also use you terminal to build nodecg-io:

```shell
cd path/to/nodecg-io
npm run build
```

To do a full rebuild instead of just an incremental build you can use
`npm run rebuild`.

The watch builder can be activated here too:

```shell
cd path/to/nodecg-io
npm run watch
```

## Run

To test the changes you simply need to start/restart NodeCG.

## Adding dependencies to packages

This project uses
[npm workspaces](https://docs.npmjs.com/cli/v7/using-npm/workspaces/) to manage
our monorepo, and most importantly link all our packages together. Because of
linking you should not use `npm install xyz --save` to add dependencies because
npm can't get the development version of internal packages like
`nodecg-io-core`. Doing so will result in an error and break the link. Instead,
you should edit the `package.json` directly using a text editor and the run
`npm install` in the repository root.

## Open a Pull Request

Once you have implemented your feature or fixed a bug push it to your fork and
start a Pull Request.

## Merge Upstream Changes

Occasionally you will want to merge changes in the upstream repository (the
official code repo) with your fork.

```shell
cd path/to/nodecg-io
git checkout main
git pull https://github.com/codeoverflow-org/nodecg-io main
```

Manage any merge conflicts, commit them, and then push them to your fork.

You may also occasionally need to merge upstream main in a pull request. To do
that make the above to update your local main branch, and then merge your local
main branch into your PR branch.

### Where to Contribute

After cloning and building the repo, check out the
[issues list](https://github.com/codeoverflow-org/nodecg-io/issues). Issues
labelled
[help wanted](https://github.com/codeoverflow-org/nodecg-io/labels/help%20wanted)
are good issues to submit a PR for. Issues labelled
[good first issue](https://github.com/codeoverflow-org/nodecg-io/labels/good%20first%20issue)
are great candidates to pick up if you are in the code for the first time. If
you are contributing significant changes, please discuss with the assignee of
the issue first before starting to work on the issue. You may also contribute to
this [documentation](docs_setup.md).

## Suggestions

We're also interested in your feedback. You can submit a suggestion or feature
request through the issue tracker. To make this process more effective, we're
asking that these include more information to help define them more clearly.

## Discussion Etiquette

In order to keep the conversation clear and transparent, please limit discussion
to English and keep things on topic with the issue. Be considerate to others and
try to be courteous and professional at all times.
