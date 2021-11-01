# Add your sample to the docs

To document a sample bundle take a look at the name of the service the sample
bundle is for. If it's for example `nodecg-io-example` the documentation should
go into `docs/samples/example.md` in the doc's repository. There you should
include a step-by-step manual how to configure the service and get the bundle
running.

!!! ATTENTION

    Don't forget to add the newly created Markdown file to `mkdocs.yml`.

!!! NOTE

    When you create your documentation pull request, please include the ID of
    your PR in the main repository in the description, so the documentation
    will not be merged before the actual code.

You should make this very detailed, so everyone gets it to work because a
super-good implementation is worth nothing if there's nobody who can use it.
Take a look at the [twitch sample bundle](../samples/twitch-chat.md).

!!! NOTE

    We also have the getting started section and especally the
    ["Try an included sample"](::/../../getting_started/try_example_bundle.md)-Guide,
    so you can offload some of the documentation to stuff aready written there.

## Guidelines

> […] The sample docs should […] be centered around the service and not the
> sample […]. Writing what the sample does with the service and how it is named
> should be enough.  
> Actually the
> [ChatOverflow docs](https://github.com/codeoverflow-org/chatoverflow-gh-pages)
> are a good example […].  
> Have a guide how to use the dashboard and then an entry for each service that
> describes what config it needs and where you can get tokens. Instead of a code
> snipped I would then explain what the sample does and link to it.
>
> ~ (daniel0611 27.02.2021 on
> [GitHub](https://github.com/codeoverflow-org/nodecg-io/issues/37#issuecomment-787054359))
> _shortened by the author_
