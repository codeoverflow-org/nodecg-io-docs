## Using the Art-Net sample bundle

The Art-Net example bundle in `samples/artnet-console` demonstrates the ability send data via Art-Net to e.g., open lighting architecture or professional lighting equipment. Here is a guide to how to get it working. The underlying service is using [`jeffreykog/node-artnet-protocol`](https://github.com/jeffreykog/node-artnet-protocol) as its library.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A working Art-Net Node in the current network

### Configure the Art-Net sample bundle

1. Start nodecg with nodecg-io installed. The artnet-console sample bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new artnet service instance using the left upper menu.

5. Enter the needed option.

    The created instance should be automatically selected, if not select it in the upper left dropdown. Enter your universe in monaco (the text-editor on the right) in this format:

    **Host**

    The broadcast address the Art-Net library will use to send `dmx` packages.

    ```json
    {
        "host": "127.0.0.1"
    }
    ```

    After entering it, click save.

    You may overwrite this broadcast address in code with `client.bind("host address");`.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created artnet service instance to the service dependency of the artnet-console bundle.

    Select the artnet-console bundle and the artnet service in the left bottom dropdown and then select the service instance that should be used by the artnet-console bundle (in this case the name of the previously created artnet instance).

7. Check the nodecg logs

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
    constructor(sequence: number, physical: number, universe: number, data: number[]);
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
    client.send(universe,
        values // number[] of values for each of the 512 channels
    );
}, 800);
```

_Note_: Since neither this library nor nodecg-io does not yet contain an abstraction, so the data is sent to the timings set by the specification, you should respect this part of specification in **your implementation**.

> However, an input that is active but not changing, will re-transmit the last valid ArtDmx
> packet at approximately 4-second intervals. (_Note_. In order to converge the needs of Art-
> Net and sACN it is recommended that Art-Net devices actually use a re-transmit time of
> 800mS to 1000mS).  
>  — [Art-Net 4 Specification p. 48](https://artisticlicence.com/WebSiteMaster/User%20Guides/art-net.pdf)
