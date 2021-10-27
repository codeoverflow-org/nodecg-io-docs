# Installation

## Prerequisites

In order to download necessary tools and to install nodecg-io using the CLI you need network access.

### Required Applications

You'll need the following tools:

-   [Git](https://git-scm.com)
-   [Node.js](https://nodejs.org/en/) v12.0.0 or newer
-   [npm](https://www.npmjs.com/get-npm) 7.0.0 or newer
-   [NodeCG](https://nodecg.dev/) 1.4.0 or newer (1.7.0 or higher recommended)

### Native Build Tools

Some services depend on packages that require native build tools. You _ONLY_ need to install these if you want to use a service that depends on native modules or if you want to install a development version.

The services that require these include StreamDeck, Midi and Serial. Please note that this list might not be up-to-date.

Here's how to install the native build tools on the most popular operating systems, if you need them:

#### Windows

For Windows, you'll need the Visual Studio Build Tools, if you have Visual Studio installed you should already have them.
If you don't have Visual Studio just install the Visual Studio Build Tools by running the following command as an **Administrator**:

```shell
npm install -g windows-build-tools
```

#### Linux

For Linux, you'll need a C++ compiler and some other packages. On Ubuntu/Debian based operating systems run the following command:

```shell
sudo apt install build-essential libusb-1.0-0-dev libasound2-dev libudev-dev
```

For other Linux distros you'll need the corresponding packages, just search on the internet how the packages are named for your specific distro.

#### macOS

For macOS, you'll need the Xcode command line tools. To install them run the following command:

```shell
xcode-select --install
```

## Install the nodecg-io CLI

Install the nodecg-io CLI using the following command:

```shell
npm install -g nodecg-io-cli
```

_Note:_ If you are running on Linux, you may need to use `sudo` if your npm installation uses a non-writeable path (default on Ubuntu apt packages, usually does not apply to packages installed using [nvm](https://github.com/nvm-sh/nvm))

## Install nodecg-io using the nodecg-io CLI

With the nodecg-io CLI installed you can run this command inside a NodeCG installation to install nodecg-io:

```shell
nodecg-io install
```

You will get a prompt which asks you which version you want to install.

-   By selecting an actual version (e.g., `0.1`) you create a production install that downloads the required packages from npm and setups a npm workspace to install all dependencies. Here you can choose which services you want to install.

-   By selecting `development` you create a development install that clones the nodecg-io git repo and builds everything from scratch. We only recommend a dev install if you are sure that you want to contribute to nodecg-io. Here you always must install all services.

For starters, we recommend using the latest non-development version.

nodecg-io will always be installed into a `nodecg-io/` directory inside your NodeCG installation so that your bundles and all bundles from nodecg-io are separated. The CLI will add this path to the loaded bundles in your NodeCG configuration automatically, you don't need to worry about it.

If you want to every change your nodecg-io installation to add/remove a service or change the version, you can always re-run `nodecg-io install`. If a nodecg-io installation is found, its options will be preselected in the prompt. Re-running `nodecg-io install` will also update all packages to the latest patch version, if you have a production installation, and pull the repository and rebuild, if you have a development installation.

## Start NodeCG

When starting NodeCG you should see that all nodecg-io related bundles should be loaded and that you can now access nodecg-io in your NodeCG dashboard.

There are many example bundles premade for most services, so you may take a
look at the [“Try an included sample”](../getting_started/try_example_bundle.md)-Guide (It
will also tell you how to log in and how to use the GUI).
Or you could directly take a deep dive into our framework and either [create a new bundle](./create_new_bundle.md)
or [integrate an existing bundle](./existing_bundle.md). There are other bundles
using nodecg-io, witch you could try, so may take a look around GitHub or GitLab.

## Uninstall nodecg-io

If you want to uninstall nodecg-io you can run the following command:

```shell
nodecg-io uninstall
```

This will remove the `nodecg-io` directory inside your NodeCG installation and also will remove it from the loaded bundle paths in your NodeCG configuration.
