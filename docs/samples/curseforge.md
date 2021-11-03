## Using the CurseForge sample bundle

The CurseForge example bundle in `samples/curseforge` demonstrates the ability
to search for different add-ons with the ID or search with specific values for
matching add-ons. Here is a guide how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

### Configure the CurseForge bundle

1. In NodeCG, create a new CurseForge service instance.
2. Set the sample's (`curseforge`) dependency to be the newly created service
   instance (of type `curseforge`).
3. Check the NodeCG logs. You should see two lists of add-ons.
