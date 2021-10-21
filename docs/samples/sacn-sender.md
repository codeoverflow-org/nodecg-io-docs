## Using the sACN sender sample bundle

The sacn-sender example bundle in `samples/sacn-sender` demonstrates the ability
send data via sACN to e.g., open lighting architecture or professional lighting
equipment. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A working sACN receiver in the current network

### Configure the sACN sample bundle

1. In NodeCG, create a new sacn-sender service instance using the left upper
   menu.
2. Enter the needed options.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your universe in monaco (the text-editor on the
    right) in this format:

    **Universes**

    The universes to use. Must be an array with numbers within 1-63999

    ```json
    {
        "universe": 1
    }
    ```

    **Port**

    Optional. The multicast port to use. All professional consoles broadcast to
    the default port 5568.

    ```json
    {
        "universes": 1,
        "port": 5568
    }
    ```

    **ReuseAddr** Optional. Allow multiple programs on your computer to listen
    to the same sACN universe.

    ```json
    {
        "universes": 1,
        "reuseAddr": true
    }
    ```

    After entering them, click save.

3. Set the created sacn-sender service instance to the service dependency of the
   sacn-sender bundle.

    Select the sacn-sender bundle and the sacn-sender service in the left bottom
    menu. Then select the service instance that should be used by the
    sacn-sender bundle (in this case the name of the previously created sACN
    instance).

4. Check the NodeCG logs

    You should see data logged.
