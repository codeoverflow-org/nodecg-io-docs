## Using the Nanoleaf sample bundle

The Nanoleaf example bundle in `samples/nanoleaf` demonstrates the ability to
control your nanoleaf lights. This example code sets all panels to an orange
colour. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   IP address of your nanoleaf controller

### Configure the nanoleaf sample bundle

1. In NodeCG, create a new nanoleaf service instance using the left upper menu.

2. Enter configuration.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your nanoleaf controller IP address in this
    format (change the IP accordingly):

    ```json
    {
        "ipAddress": "xxx.xxx.xxx.xxx"
    }
    ```

    Before clicking save put your nanoleaf controller into pairing mode by
    holding the on-off button for 5-7 seconds till the LED starts flashing.

    After entering your config and entering pairing mode, click save.

3. Set the created nanoleaf service instance to the service dependency of the
   nanoleaf sample bundle.

    Select the nanoleaf sample bundle and the nanoleaf service in the left
    bottom menu. Then select the service instance that should be used by the
    nanoleaf sample bundle (in this case the name of the previously created
    nanoleaf instance).

4. If everything worked, your nanoleafs should now shine orange.

    If not you should check the NodeCG logs for any errors.
