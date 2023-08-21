## Using the GameTTS sample bundle

The GameTTS example bundle in `samples/gametts` demonstrates the ability
to play a tts generated audio in a graphic. Here is a guide
to how to get it working.

Note that GameTTS only supports german voices.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   a GameTTS Server Instance
    

!!! NOTE

    GameTTS can be found at https://github.com/lexkoro/GameTTS.
    A docker image of GameTTS is available on docker hub at `henrikhansen/gametts:latest`.

    Here's an example docker compose file to get it working:

    ```yaml
    version: '3'
      
    services:
      gametts:
        image: henrikhansen/gametts:latest
        restart: always
        ports:
          - 5000:5000
        container_name: gametts
        volumes:
          - ./gametts:/usr/src/app/GameTTS/vits/model/
    ```

### Configure the GameTTS sample bundle

1. In NodeCG, create a new gametts service instance.

2. Enter your host information like this

    ```json
    {
        "host": "example.com:12345",
        "useHttps": false
    }
    ```

    After entering it, click save.

3. Set the sample's (`gametts`) dependency to be the newly created service
   instance (of type `gametts`).

4. Open the GameTTS sample bundle graphic:

    You should hear "Hallo aus nodecg-io!" using a random TTS voice.
