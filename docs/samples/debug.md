## Using the Debug sample bundle

The Debug Helper example bundle in `samples/debug` demonstrates the ability to
use the debug helper to send same sample data to your bundle, so you can trigger
different features and test/debug them.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

### Configure the Debug sample bundle

1. In NodeCG, create a new Debug service instance.
2. Set the sample's (`debug`) dependency to be the newly created service
   instance (of type `debug`).
3. Go to the nodecg-io-debug dashboard and use some buttons or other inputs.
4. Check the NodeCG log. It should contain a message for each action you did and
   the passed values.
