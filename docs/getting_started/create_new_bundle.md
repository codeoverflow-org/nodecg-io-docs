# Create your first bundle

To actually use nodecg-io you need to create a bundle. Here's a step-by-step guide to create one.

Think of what services your bundle needs. Take a look at the [service list](../services.md) if to see what services are available. If you need a service that is not yet available consider [creating it](../contribute/create_service.md).

## Create your bundle using the nodecg-io CLI

Automatically generating a bundle that uses nodecg-io requires that you have the nodecg-io CLI installed. A guide on how to do this is inside the [installation guide](./install.md). Also note that this currently only works when you have installed a release version, not development versions.

To start run this command while being inside your nodecg installation:

```shell
nodecg-io generate
```

This will ask you a couple details about your bundle like name, description and used services.
Most questions have a reasonable default that you can choose if you don't care or are not sure about the asked thing.

After finishing the prompt the CLI will generate your bundle, install dependencies and, if you have chosen TypeScript, compile the generated code.

## Test it

Start NodeCG and make sure that the bundle gets loaded successfully, and it is displayed in the nodecg-io dashboard with all service dependencies.

## Modify it

After that you should edit the `extension/index.ts` or `extension/index.js` depending on your chosen language to do something useful.
You can start by updating the `onAvailable` callbacks.

_Note:_ If you need to access another service inside the callback of a `onAvailable` call you can use `otherService.getClient()` to get the client or `undefined` if it is not set.

## Further steps

A couple of steps you may want to do after generating a bundle:

-   Create a git repository for you bundle (a `.gitignore` is automatically generated for you) and push it to a git platform of your choice
-   Add an [open source licence](https://choosealicense.com), don't forget it to also add it to the `package.json` file
-   Add code formatters and linting tools like [prettier](https://prettier.io/) and [ESLint](https://eslint.org/)
-   Add a README that explains what your bundle does and how it can be used

## Share it!

If you share your work others might find it useful and get happy with it. We made nodecg-io for you, and the nodecg people made nodecg for you. Many people spent much time for you to create cool content that easy and if you shared your work others could create good content more easily as well.
