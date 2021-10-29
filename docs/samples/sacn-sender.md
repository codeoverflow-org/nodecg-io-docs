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

1. In NodeCG, create a new sacn-sender service instance.
2. Enter the needed options:

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

3. Set the sample's (`sacn-sender`) dependency to be the newly created service
   instance (of type `sacn-sender`).

4. Check the NodeCG logs:

    You should see data logged.
