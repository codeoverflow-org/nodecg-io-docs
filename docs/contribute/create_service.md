# Create a service integration

This guide helps you to create a service integration such as _twitch-chat_ or _discord_

## Find a javascript library

Go to [npmjs.com](https://www.npmjs.com/) and look whether there's already a package that wraps around the API of your service. If there's no such package you need to create one yourself. This process is not described here.

## Create a package

From here you will have to replace:

-   `YourServiceName` to your service's name in [PascalCase](https://github.com/basarat/typescript-book/blob/master/docs/styleguide/styleguide.md#class).
-   `yourServiceName` to your service's name in [carmelCase](https://github.com/basarat/typescript-book/blob/master/docs/styleguide/styleguide.md#variable-and-function).
-   `your-service-name` to your service's name with only lowercase and hyphens ( `-` ) for example: ws-server.

Now you need to create a package. You should call it `nodecg-io-your-service-name`.

First create a directory with that name put file called `package.json` into it.

Put the following into it:

```json
{
    "name": "nodecg-io-<your-service-name>",
    "version": "0.1.0",
    "description": "<Short description what is possible with your service.>",
    "homepage": "https://nodecg.io/samples/<your-service-name>",
    "author": {
        "name": "<Your name>",
        "url": "<Your github profile url>"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/codeoverflow-org/nodecg-io.git",
        "directory": "nodecg-io-<your-service-name>"
    },
    "main": "extension",
    "scripts": {
        "build": "tsc -b",
        "watch": "tsc -b -w",
        "clean": "tsc -b --clean"
    },
    "keywords": ["nodecg-io", "nodecg-bundle"],
    "nodecg": {
        "compatibleRange": "^1.1.1",
        "bundleDependencies": {
            "nodecg-io-core": "^0.1.0"
        }
    },
    "license": "MIT",
    "devDependencies": {
        "@types/node": "^14.14.13",
        "nodecg": "^1.7.4",
        "typescript": "^4.1.3"
    },
    "dependencies": {
        "nodecg-io-core": "^0.1.0",
        "<the package you found in step 1>": "<the packages version you want to use>"
    }
}
```

Next you need to put a file called `tsconfig.json` next to your `package.json`. The `tsconfig.json` should look like this:

```json
{
    "extends": "../tsconfig.common.json"
}
```

Now run `npm install` and `npm run bootstrap` in the repository root.

## Create a configuration schema

Next create a file called `your-service-name-schame.json`. This is a json schema file that indicates how the configuration for your service should be structured. If you need help here take a look at [this](https://json-schema.org/understanding-json-schema/) online resource and the schema-files of the other service implementations.

## Create the service

Create a file called `index.ts` in a folder called `extension` inside your services directory. You can then paste the following code and fill in your code instead of the comments.

```typescript
// TODO: Rename all occurences of "YourServiceName" in PascalCase
// TODO: Rename all occurences of "yourServiceName" in carmelCase
// TODO: Rename all occurences of "your-service-name" with only lowercase and hyphens ( - )

import { NodeCG } from "nodecg/types/server";
import { Result, emptySuccess, success, ServiceBundle, ServiceClient } from "nodecg-io-core";
// TODO: Replace the "fake" service class with that found on npm etc.
import { ServiceClass } from "./";

interface YourServiceNameServiceConfig {
    // TODO Fill in the values from your json schema here. The json
    // schema will load into an instance of this.
}

// ServiceClient ensures that you will provide a `getNativeClient` function that should give
// access to the underlying client from the library that you are using.
// TODO: if you want to provide simplifications for the service then make this
// type-alias a separate class in a separate file and directly implement those simplifications
// there.
// TODO: Replace the `ServiceClass` with the class of the package from step 1
export type YourServiceNameServiceClient = ServiceClient<ServiceClass>;

module.exports = (nodecg: NodeCG) => {
    new YourServiceNameService(nodecg, "your-service-name", __dirname, "../your-service-name-schema.json").register();
};

class YourServiceNameService extends ServiceBundle<YourServiceNameServiceConfig, YourServiceNameServiceClient> {
    async validateConfig(config: YourServiceNameServiceConfig): Promise<Result<void>> {
        // TODO You can validate your config here. If this gets called, the schema is correct.
        // You should for example check whether oauth keys are valid and servers are online here
        // If everything is good return 'emptySuccess()'
        // If an error occurs return 'error(<The error message>)'
    }

    async createClient(config: YourServiceNameServiceConfig): Promise<Result<YourServiceNameServiceClient>> {
        // TODO Here you should return a <Your service name>ServiceClient that is exposed to bundles.
        // If everything is good return 'success({
        //     getNativeClient() {
        //         return <The raw client from the package from step 1>
        //     }
        // })'
        // Or create a instance of your class if you have any simplifications and return that.
        // If an error occurs return 'error(<The error message>)'
    }

    stopClient(client: YourServiceNameServiceClient): void {
        // Here you shuld make sure you disconnect everything here (if possible).
    }
}
```

Now run `npm run build` in the repository root, start NodeCG and test your service out.

## Next steps

You could [create a sample bundle](create_sample.md) for your brand-new service.

If you don't do so, make sure you add a placeholder file called `<the services name>.md` in `docs/samples` in your fork of the documentation.

The file should look like this:

```markdown
<!-- Marker for build.py that there's no sample bundle. Remove this if you created one -->

## Using the <the services name> sample bundle

No sample bundle for service `<the services name>`.  
[You can help us and create one!](https://github.com/codeoverflow-org/nodecg-io/blob/master/docs/docs/contribute.md)
```

Do not remove the marker in the first line until the bundle is implemented and don't forget to add this file to `mkdocs.yml`.
