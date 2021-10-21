## Using the IntelliJ sample bundle

The IntelliJ example bundle in `samples/intellij-integration` Shows how to
connect to a JetBrains IDE and print all installed plugins. Here is a guide to
how to get it working:

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

1. Clone [this](https://github.com/noeppi-noeppi/nodecg-io-intellij) Git
   Repository.
2. Make sure you've Java 11 or newer installed.
3. Run `gradlew build` (on Windows) or `./gradlew build` (on Linux) inside the
   cloned repository.
4. Inside your JetBrains IDE go to `Settings` and then `Plugins`. Click on the
   little gear in the top right corner. Then click `Install from file`.
5. Navigate to `path to your cloned repository/build/libs` and select the jar
   file there.
6. Restart the IDE.

### Configure the IntelliJ sample bundle

1. In NodeCG, create a new IntelliJ service instance using the left upper menu.

2. Enter the following

    ```
    {
        "address": "127.0.0.1:19524"
    }
    ```

    This tells nodecg-io to look for your IDE's HTTP server on your computer at
    port `19524`. If you want it to run on another port, please follow the
    guidelines
    [here](https://github.com/noeppi-noeppi/nodecg-io-intellij/blob/master/README.md).

3. Set the created IntelliJ service instance to the service dependency of the
   sample-intellij bundle.

    Select the sample-intellij bundle and the IntelliJ service in the left
    bottom menu. Then select the service instance that should be used by the
    sample-intellij bundle (in this case the name of the previously created
    IntelliJ instance).

4. Check the NodeCG logs

    You should see an error or a list of all plugins installed at your IDE
    including the preinstalled ones by JetBrains.
