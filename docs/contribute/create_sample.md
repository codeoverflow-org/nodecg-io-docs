# Create a sample bundle

Create a folder in `samples` and add a `package.json` and a `tsconfig.json`:

```json
{
  "name": "<the samples name>",
  "version": "0.1.0",
  "nodecg": {
    "compatibleRange": "^1.1.1",
    "bundleDependencies": {
      "nodecg-io-intellij": "0.1.0"
    }
  },
  "scripts": {
    "build": "tsc",
    "watch": "tsc -w"
  },
  "license": "MIT",
  "dependencies": {
    "nodecg-io-<the services name>": "0.1.0",
    "nodecg-io-core": "0.1.0",
    "@types/node": "^13.13.5",
    "nodecg": "^1.6.1",
    "typescript": "^3.8.3"
  }
}
```

```json
{
  "extends": "../../tsconfig.common.json"
}
```

Now you can create file called `extension/index.ts`. Here's a template. Make sure you replace all the comments with your own code.

```typescript
import { NodeCG } from "nodecg/types/server";
import { ServiceProvider } from "nodecg-io-core/extension/types";
import { <the services exported client> } from "nodecg-io-<the services name>/extension";

module.exports = function (nodecg: NodeCG) {
    nodecg.log.info("Sample bundle for <the services name> started");

    // This explicit cast determines the client type in the requireService call
    const service = (nodecg.extensions["nodecg-io-twitch"] as unknown) as
        | ServiceProvider<TwitchServiceClient>
        | undefined;

    service?.requireService(
        "<sample-service>",
        (client) => {
            nodecg.log.info("Client has been updated.");

            // TODO do something with the client to demonstrate the functionality.
        },
        () => nodecg.log.info("Client has been unset."),
    );
};
```

## Next steps

You could [add documentation](create_sample.md) for the sample bundle.