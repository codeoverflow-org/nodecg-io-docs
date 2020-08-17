# Create a sample bundle

Create a folder in `samples` and add a `package.json` and a `tsconfig.json`:

```json
{
    "name": "<the samples name>",
    "version": "0.1.0",
    "nodecg": {
        "compatibleRange": "^1.1.1",
        "bundleDependencies": {
            "nodecg-io-<the service name>": "0.1.0"
        }
    },
    "scripts": {
        "build": "tsc",
        "watch": "tsc -w"
    },
    "license": "MIT",
    "dependencies": {
        "nodecg-io-<the service name>": "0.1.0",
        "nodecg-io-core": "0.1.0",
        "@types/node": "^13.13.12",
        "nodecg": "^1.6.1",
        "typescript": "^3.9.6"
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
import { requireService } from "nodecg-io-core/extension/serviceClientWrapper";
import { TheServicesExportedClient } from "nodecg-io-<the services name>/extension";

module.exports = function(nodecg: NodeCG) {
    nodecg.log.info("Sample bundle for <the-service-name> started");

    const service = requireService<TheServicesExportedClient>(
        nodecg,
        "<the-service-name>"
    );
    service?.onAvailable((client) => {
        nodecg.log.info("Client has been updated.");

        // TODO do something with the client to demonstrate the functionality.
    });

    service?.onUnavailable(() => nodecg.log.info("Client has been unset."));
};
```

## Next steps

You could [add documentation](create_sample.md) for the sample bundle.
