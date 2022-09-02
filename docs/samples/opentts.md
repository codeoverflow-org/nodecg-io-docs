## Using the OpenTTS sample bundle

The OpenTTS example bundle in `samples/opentts` demonstrates the ability
to play a tts generated audio in a graphic. Here is a guide
to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   a OpenTTS Server Instance

!!! NOTE

    If you don't have a OpenTTS Server Instance you can create one with Docker.
    Read [here](https://github.com/synesthesiam/opentts#running) for more information.

### Configure the OpenTTS sample bundle

1. In NodeCG, create a new opentts service instance.

2. Enter your host information like this

    ```json
    {
        "host": "example.com:12345",
        "useHttps": false
    }
    ```

    After entering it, click save.

3. Set the sample's (`opentts`) dependency to be the newly created service
   instance (of type `opentts`).

4. Open the OpenTTS sample bundle graphic:

    You should hear "hello world" using a random TTS voice.
