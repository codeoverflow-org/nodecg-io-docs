# Installation

## Prerequisites

In order to download necessary tools, clone the repository, and install dependencies via `npm` you need network access.

You'll need the following tools:

-   [Git](https://git-scm.com)
-   [Node.JS](https://nodejs.org/en/) v12.0.0 or newer
-   [Npm](https://www.npmjs.com/get-npm)
-   [NodeCG](https://nodecg.com/)

You'll also need operating system dependant tools for native modules like Streamdeck and Midi:

### Windows

For Windows you'll need the Visual Studio Build Tools, if you have Visual Studio installed you should already have them.
If you don't have Visual Studio just install the Visual Studio Build Tools by running the following command as an __Administrator__:

```shell
npm install -g windows-build-tools
```

### Linux

For Linux you'll need a C++ compiler and some other packages. On Ubuntu/Debian based operating systems run the following command:

```shell
sudo apt install build-essentials libusb-1.0-0-dev libasound2-dev libudev-dev
```

For other linux distros you'll need the corresponding packages, just search on the internet how the packages are named for your specific distro.

### MacOS

For MacOS you'll need the Xcode command line tools. To install them run the following command:

```shell
xcode-select --install
```

## Clone this repository:

```shell
git clone https://github.com/codeoverflow-org/nodecg-io.git
```

_Note:_ You should clone nodecg-io to somewhere outside of your nodecg bundles/ directory as this repo contains many bundles in subdirectories and nodecg doesn't support nesting of the bundles in other directories. You can clone it to any other path that you wish.

## Install all of the dependencies using `npm`:

```shell
cd path/to/nodecg-io
npm install
npm run bootstrap
```

## Build nodecg-io:

```shell
cd path/to/nodecg-io
npm run build
```

## Add nodecg-io directory to the nodecg config:

Modify the nodecg configuration in `path/to/nodecg/cfg/nodecg.json`, here is an example config:

```json
{
    "bundles": {
        "paths": ["path/to/nodecg-io", "path/to/nodecg-io/samples"]
    }
}
```

_Note 1:_ This path should point to the root of this repository, not to a bundle inside this repo.

_Note 2:_ The second path to the samples is only required if you want to use a sample plugin.

_Note 3:_ If nodecg doesn't load nodecg-io for some reason you might want to use an absolute path here.

## Start nodecg

Now you can use nodecg-io in your own bundle. You can find example code in [./samples/](https://github.com/codeoverflow-org/nodecg-io/tree/master/samples/).
