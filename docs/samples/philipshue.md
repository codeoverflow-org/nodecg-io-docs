## Using the Philips Hue sample bundle

The philipshue-lights example bundle in `samples/philipshue-lights` demonstrates
the ability to connect to the Philips Hue bridge and control Philips Hue
accessories.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Philips Hue bridge with some connected accessories

### Configure the Philips Hue sample bundle

1. In NodeCG, create a new Philips Hue service instance using the left upper
   menu.

2. Enter configuration for hue.

    The created instance should be automatically selected, if not select it in
    the upper left menu. If you want the bridge to be automatically discovered
    just set `discover` to true like this:

    ```json
    {
        "discover": true
    }
    ```

    If you want to provide the IP address manually you can provide them like
    this:

    ```json
    {
        "discover": false,
        "ipAddr": "x.x.x.x"
    }
    ```

    After entering it, press the big link button on your bridge and then click
    save.

    After the first time you connect to your bridge it will create a user and an
    API key which will be saved so that you only need to press the link button
    when you connect it for the first time.

3. Set the created Philips Hue service instance to the service dependency of the
   philipshue-lights sample bundle.

    Select the philipshue-lights sample bundle and the Philips Hue service in
    the left bottom menu. Then select the service instance that should be used
    by the philipshue-lights sample bundle (in this case the name of the
    previously created Philips Hue instance).

4. Check the NodeCG logs

    You should see an error or a success message and the number of lights that
    the bridge knows of.
