# Add your sample to the docs

To document a sample bundle take a look at the name of the service the sample bundle is for. If it's for example `nodecg-io-example` the documentation must go into `docs/samples/example.md` in the docs repository. There you should include a step-by-step manual how to configure the service and get the bundle running.

Don't forget to add the newly created MarkDown file to `mkdocs.yml`. When you create your documentation pull request, please include the id of your PR in the main repository in the description so the documentation is not merged before the actual code.

You should make this very detailed so everyone gets it to work because a super-good implementation is worth nothing if there's nobody who can use it. Take a look at the [twitch sample bundle](../samples/twitch.md).
