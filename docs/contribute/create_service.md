# Create a service integration

This guide helps you to create a service integration such as *twitch-chat* or *discord*

## Find a javascript library

Go to [npmjs.com](https://www.npmjs.com/) and look whether there's already a package that wraps around the API of your service. If there's no such package you need to create one yourself. This process is not described here.

## Create a package

Now you need to create a package. You should call it `nodecg-ui-<your service name>`.

First create a directory with that name put file called `package.json` into it.

Put the following into it: 

```json
{
  "name": "nodecg-io-<your service name>",
  "version": "0.1.0",
  "description": "<Short description what is possible with your service.>",
  "homepage": "",
  "author": {
    "name": "<Your name>",
    "url": "<Your github profile url>"
  },
  "scripts": {
    "build": "tsc",
    "watch": "tsc -w"
  },
  "keywords": [
    "",
    "nodecg-bundle"
  ],
  "nodecg": {
    "compatibleRange": "^1.1.1",
    "bundleDependencies": {
      "nodecg-io-core": "0.1.0"
    }
  },
  "license": "MIT",
  "devDependencies": {
    "@types/node": "^13.13.5",
    "nodecg": "^1.6.1",
    "typescript": "^3.8.3"
  },
  "dependencies": {
    "nodecg-io-core": "0.1.0",
    "<the package you found in step 1>": "<the packages version you wan't to use>"
  }
}
```

Next you need to put a file called `tsconfig.json` next to your `package.json`. The `tsconfig.json` should look like this:

```json
{
  "extends": "../tsconfig.common.json"
}
```

Now run `npm install` in the repository root.

## Create a configuration schema

Next create a file called `<your service name>-schame.json`. This is a json schema file that indicates how the configuration for your service should be structured. If you need help here take a look at [this](https://json-schema.org/understanding-json-schema/) online resource and the schema-files of the other service implementations.

## Create the service

Create a file called `index.ts` in a folder called `extension` inside your services directory. You can then paste the following code and fill in your code instead of the comments.

```typescript
import { NodeCG } from "nodecg/types/server";
import { NodeCGIOCore } from "nodecg-io-core/extension";
import { Service, ServiceProvider } from "nodecg-io-core/extension/types";
import { emptySuccess, success, error, Result } from "nodecg-io-core/extension/utils/result";

interface <Your service name>ServiceConfig {
    // TODO Fill in the values from your json schema here. The json
    // schema will load into an instance  of this.
}

export interface <Your service name>ServiceClient {
    // This interface is exposed to bundles. Make shure it's no longer
    // possible to access the login credentials from here
    getRawClient(): <class of the package from step 1 taht should be exposed to bundles>;
}

module.exports = (nodecg: NodeCG): ServiceProvider<<Your service name>ServiceClient> | undefined => {
    nodecg.log.info("<Your service name> bundle started");
    const core = (nodecg.extensions["nodecg-io-core"] as unknown) as NodeCGIOCore | undefined;
    if (core === undefined) {
        nodecg.log.error("nodecg-io-core isn't loaded! <Your service name> bundle won't function without it.");
        return undefined;
    }

    const service: Service<<Your service name>ServiceConfig, <Your service name>ServiceClient> = {
        schema: core.readSchema(__dirname, "../<Your service name>-schema.json"),
        serviceType: "<Your service name>",
        validateConfig: validateConfig,
        createClient: createClient(nodecg),
        stopClient: stopClient,
    };

    return core.registerService(service);
};

async function validateConfig(config: <Your service name>ServiceConfig): Promise<Result<void>> {
    // TODO You can validate your config here. If this gets called, the schema is correct.
    // You should for example check whether oauth keys are valid and servers are online here
    // If everything is good return 'emptySuccess()'
    // If an error occurs return 'error(<The error message>)'
}

function createClient(nodecg: NodeCG): (config: TwitchServiceConfig) => Promise<Result<TwitchServiceClient>> {
    return async (config) => {
        // TODO Here you should return a <Your service name>ServiceClient that is exposed to bundles.
        // If everything is good return 'success({
        //     getRawClient() {
        //         return <The raw client from the package from step 1>
        //     }
        // })'
        // If an error occurs return 'error(<The error message>)'
    };
}

function stopClient(client: TwitchServiceClient): void {
    // At the moment this does not work but it will in the future so make shure you disconnect everything here.
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

Do not remove the marker in the first line until the bundle is implemented and on't forget to add this file to `mkdocs.yml`.