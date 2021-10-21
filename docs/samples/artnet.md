## Using the Art-Net sample bundle

The Art-Net example bundle in `samples/artnet-console` demonstrates the ability
send data via Art-Net to e.g., open lighting architecture or professional
lighting equipment. Here is a guide to how to get it working. The underlying
service is using
[`jeffreykog/node-artnet-protocol`](https://github.com/jeffreykog/node-artnet-protocol)
as its library.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A working Art-Net Node in the current network

### Configure the Art-Net sample bundle

1. In NodeCG, create a new Art-Net service instance using the left upper menu.
2. Enter the needed option.

    The created instance should be automatically selected, if not select it in
    the upper left dropdown. Enter your universe in monaco (the text-editor on
    the right) in this format:

    **Host**

    The broadcast address the Art-Net library will use to send `dmx` packages.

    ```json
    {
        "host": "127.0.0.1"
    }
    ```

    After entering it, click save.  
    You may overwrite this broadcast address in code with
    `client.bind("host address");`.

3. Set the created Art-Net service instance to the service dependency of the
   artnet-console bundle.  
   Select the artnet-console bundle and the Art-Net service in the left bottom
   dropdown and then select the service instance that should be used by the
   artnet-console bundle (in this case the name of the previously created
   Art-Net instance).

4. Check the NodeCG logs  
   You should see data logged.

### Explanations

#### Receiving DMX data

```ts
client.onDMX((dmx) => {
    // dmx contains an ArtDmx object
    nodecg.log.info(dmx.universe, dmx.data);
});
```

The data you receive has the following fields:

```ts
declare class ArtDmx {
    opcode: number;
    protocolVersion: number;
    sequence: number;
    physical: number;
    universe: number;
    data: number[];
    constructor(
        sequence: number,
        physical: number,
        universe: number,
        data: number[]
    );
    isSequenceEnabled(): boolean;
    static decode(data: Buffer): ArtDmx;
    toString(): string;
    encode(): Buffer;
}
```

#### Sending DMX data

```ts
// send new data every 0,8 seconds.
// This is the official timing for re-transmiting data in the artnet specifciation.
setInterval(() => {
    client.send(
        universe,
        values // number[] of values for each of the 512 channels
    );
}, 800);
```

_Note_: Since neither this library nor nodecg-io does not yet contain an
abstraction, so the data is sent to the timings set by the specification, you
should respect this part of specification in **your implementation**.

> However, an input that is active but not changing, will re-transmit the last
> valid ArtDmx packet at approximately 4-second intervals. (_Note_. In order to
> converge the needs of Art- Net and sACN it is recommended that Art-Net devices
> actually use a re-transmit time of 800mS to 1000mS).  
>  — [Art-Net 4 Specification p. 48](https://artisticlicence.com/WebSiteMaster/User%20Guides/art-net.pdf)
