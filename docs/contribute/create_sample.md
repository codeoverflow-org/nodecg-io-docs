# Create a sample bundle

A sample should have the same name as the service but it may include a short description in the name after the service name aswell.
E.g. `twitch-chat` or `obs-scenelist`.

Create a folder in `samples` named after the sample and add a `package.json` and a `tsconfig.json`:

```json
{
    "name": "<the sample name>",
    "private": true,
    "version": "0.1.0",
    "nodecg": {
        "compatibleRange": "^1.1.1",
        "bundleDependencies": {
            "nodecg-io-<the service name>": "^0.1.0"
        }
    },
    "scripts": {
        "build": "tsc -b",
        "watch": "tsc -b -w",
        "clean": "tsc -b --clean"
    },
    "license": "MIT",
    "dependencies": {
        "nodecg-io-<the service name>": "^0.1.0",
        "nodecg-io-core": "^0.1.0",
        "@types/node": "^14.14.13",
        "nodecg": "^1.7.4",
        "typescript": "^4.1.3"
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
import { requireService } from "nodecg-io-core";
import { TheServicesExportedClient } from "nodecg-io-<the services name>";

module.exports = function (nodecg: NodeCG) {
    nodecg.log.info("Sample bundle for <the-service-name> started");

    const service = requireService<TheServicesExportedClient>(nodecg, "<the-service-name>");
    service?.onAvailable((client) => {
        nodecg.log.info("Client has been updated.");

        // TODO do something with the client to demonstrate the functionality.
    });

    service?.onUnavailable(() => nodecg.log.info("Client has been unset."));
};
```

## Next steps

You could [add documentation](create_sample.md) for the sample bundle.
