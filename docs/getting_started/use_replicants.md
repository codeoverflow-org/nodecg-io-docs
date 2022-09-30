# Use service replicants

Some services allow reading some data using [NodeCG Replicants](https://www.nodecg.dev/docs/classes/replicant).

Replicants are especially useful for displaying simple information in graphics and dashboards.
You can setup a replicant and directly use it for basic values inside your graphic/dashboard without the need for much extension code.

TODO: explain for what replicants are useful

Current list of services with replicant support:

-   StreamElements

(more services with replicants will hopefully be added in the future)

## Create and register replicants in your bundle extension

To use a replicant of a service you must first depend on the service as usual.
Please refer to [Your first bundle](./create_new_bundle.md) and [Migrating an existing bundle](./existing_bundle.md) for a guide on how to depend on nodecg-io services inside your NodeCG extension.

With access to a service client you can create a replicant inside your bundle and pass it to the `setupReplicant` method of the service client to let it be filled with data by the service.
Here's an example for the StreamElements service (replace the name with the service of the above list that you want to use):

=== "TypeScript"

    ```typescript
    // Update your imports to include the type of the replicant data:
    import { StreamElementsReplicant, StreamElementsServiceClient } from "nodecg-io-streamelements";

    module.exports = function(nodecg: NodeCG) {
        // Require service (as usual)
    	const streamElements = requireService<StreamElementsServiceClient>(nodecg, "streamelements");

        // Define replicant
        const streamElementsReplicant = nodecg.Replicant<StreamElementsReplicant>("myStreamElementsReplicant");

        ...

        streamElements?.onAvailable((client) => {
            ...
            // Connect your replicant to this nodecg-io service instance.
            client.setupReplicant(streamElementsReplicant);
        });
    }
    ```

=== "JavaScript"

    ```javascript
    module.exports = function(nodecg: NodeCG) {
        // Require service (as usual)
        const streamElements = requireService(nodecg, "streamelements");

        // Define replicant
        const streamElementsReplicant = nodecg.Replicant("myStreamElementsReplicant");

        ...

    streamElements?.onAvailable((client) => {
            ...
        // Connect your replicant to this nodecg-io service instance.
        client.setupReplicant(streamElementsReplicant);
    });
    }

    ```

## Use the service replicant

In case you want to use the created replicant in your bundles extension you already have it declared and a reference to it in a variable. If you want to use it in a graphic or dashboard you'll need to declare the replicant with the same name there too.

You can access the NodeCG replicant as usual. Use `replicant.value` to get the current state and `replicant.on("change", (newValue, oldValue) => { /* .... */ })` to be informed when the value of the replicant changes.

To figure out what properties are available on the object value you can either look at the corresponding sample bundle or use autocomplete in your editor if you're using TypeScript.
