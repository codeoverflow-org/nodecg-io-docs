nodecg-io has a steadily growing and improving documentation. We are using
[Markdown](https://en.wikipedia.org/wiki/Markdown) to describe the content and
mkdocs for the deployment to the webpage (<https://nodecg.io>). If you want to
get to know the standard Markdown syntax, take a look at this
[guide](https://www.markdownguide.org/). We also use many plugins, so you may
take a look at a curated list of [examples](docs_markdown.md) of the extended syntax.

## Clone this repo

If you installed the development version nodecg-io with the CLI, you may have already cloned the `nodecg-io-docs` repository into the `docs` folder inside nodecg-io directory. Then you will have to fork the official repo and add your fork as a remote:

```shell
git remote add <name> (https://github.com/<your-user-name>/nodecg-io-docs.git)
```

Else clone your fork into a desired directory with:

```shell
git clone https://github.com/<your-user-name>/nodecg-io-docs.git
```

## Repository structure

```plain
|-- .github ................ CI workflows
|-- .vscode ................ VS Code specific configs
|-- docs ................... All files included in the documentation
|   |-- assets ................ other files used (images)
|   |-- contribute ............ Section on development and documentation
|   |-- getting_started ....... Section on first use
|   |-- samples ............... documentation for the sample bundles
|   |-- dependencies.md ....... One huge UML diagram (auto generated)
|   |-- index.md .............. Home screen of the documentation
|   `-- services.md ........... Availabel Services (auto generated)
|-- .markdownlint.json ..... markdownlint config file
|-- .prettierrc.json ....... prettier (formatter) config file
`-- mkdocs.yml ............. mkdocs config file
```

## Install dependencies to use the preview

You will need a Python 3 installed. You will also need to install mkdocs with pip:

```shell
pip install -r requirements.txt
```

Now you can serve the local version with:

```shell
mkdocs serve
```

Now you can access it in your browser under <http://127.0.0.1:8000/>.

## Using VS Code

### Extensions

For the folks out there who are using VS Code to edit these documents you can use
the recommended extensions of this workspace by using the `@recommended ` filter
in the extensions panel. Those extensions will format (`Prettier`) and lint
(`markdownlint`) the markdown files, and live check many typos and grammar
(`LTeX`). Also, the built-in preview will parse more of our used syntax.

### Tasks

!!! NOTE

    You will need prettier and markdownlint installed in your path.

You may also benefit from the preconfigured serve task. It can be accessed with <kbd>Ctrl</kbd> +
<kbd>Shift</kbd> + <kbd>B</kbd> (<kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>B</kbd>
on macOS). This will format and lint the files and then serve them to you.
