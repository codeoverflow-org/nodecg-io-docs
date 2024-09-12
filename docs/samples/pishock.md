## Using the PiShock sample bundle

The PiShock example bundle in `samples/pishock` demonstrates the ability
to use the PiShock api to get the infos about the shockers. Here is a guide
to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   1 PiShock Hub
-   At least 1 Shocker
-   An PiShock Account

### Configure the PiShock sample bundle

1. In NodeCG, create a new pishock service instance.

2. Enter your authentication details like this

   ```json
   {
       "authentications": [
           {
               "username": "myAwesomeUsername",
               "apiKey": "12345678-1234-1234-1234-123456789012",
               "code": "ABCDEFGHIJK",
               "name": "nodecg-io-pishock-integration"
           }
       ]
   }
   ```

   Multiple authentications may be provided to allow the using bundle
   to access multiple devices.
   Setting the client name is optional and defaults to `nodecg-io PiShock Service` if none is provided.
   After entering it, click save.

3. Set the sample's (`pishock`) dependency to be the newly created service
   instance (of type `pishock`).

4. View the NodeCG console log which should contain all information about the provided devices
