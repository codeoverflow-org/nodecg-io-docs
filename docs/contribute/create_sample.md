# Create a sample bundle

A sample should have the same name as the service, but it may include a short description in the name after the service name as well.
E.g. `twitch-chat` or `obs-scenelist`.

Create a folder in `samples` named after the sample and add a `package.json` and a `tsconfig.json`:

```json
{
    "name": "<the sample name>",
    "private": true,
    "version": "0.2.0",
    "nodecg": {
        "compatibleRange": "^1.1.1",
        "bundleDependencies": {
            "nodecg-io-<the service name>": "^0.2.0"
        }
    },
    "scripts": {
        "build": "tsc -b",
        "watch": "tsc -b -w",
        "clean": "tsc -b --clean"
    },
    "license": "MIT",
    "dependencies": {
        "nodecg-io-<the service name>": "^0.2.0",
        "nodecg-io-core": "^0.2.0",
        "@types/node": "^15.0.2",
        "nodecg-types": "^1.8.2",
        "typescript": "^4.2.4"
    }
}
```

```json
{
    "extends": "../../tsconfig.common.json"
}
```

Now you can create a file called `extension/index.ts`. Here's a template. Make sure you replace all the comments with your own code.

```typescript
import { NodeCG } from "nodecg-types/types/server";
import { requireService } from "nodecg-io-core";
import { TheServicesExportedClient } from "nodecg-io-<the services name>";

module.exports = function (nodecg: NodeCG) {
    nodecg.log.info("Sample bundle for <the-service-name> started");

    const service = requireService<TheServicesExportedClient>(
        nodecg,
        "<the-service-name>"
    );
    service?.onAvailable((client) => {
        nodecg.log.info("<the-service-name> client has been updated.");

        // TODO do something with the client to demonstrate the functionality.
    });

    service?.onUnavailable(() =>
        nodecg.log.info("<the-service-name> client has been unset.")
    );
};
```

## Next steps

You could [add documentation](create_sample.md) for the sample bundle.
