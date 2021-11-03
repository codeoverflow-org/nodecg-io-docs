Our special mix of Markdown plugins:

## [`plantuml-markdown`](https://github.com/mikitex70/plantuml-markdown)

!!! EXAMPLE "Plant UML diagram"

    === "Markdown"

        ````markdown
        ```plantuml format="svg" alt="My super  diagram placeholder"   width="400px"  height="400px"
        title Authentication Sequence
        Alice ->  Bob: calls
        Alice <-- Bob: responds
        ```
        ````

    === "Output"

        ```plantuml format="svg" alt="My super  diagram placeholder"   width="400px"  height="400px"
        title Authentication Sequence
        Alice ->  Bob: calls
        Alice <-- Bob: responds
        ```

## [`codehilite`](https://python-markdown.github.io/extensions/code_hilite/)

Syntax highlighting in fenced code blocks.

!!! EXAMPLE "Syntax highlighting"

    === "Markdown"

        ````markdown
        ```typescript
        import { NodeCG } from "nodecg-types/types/server";
        module.exports = (nodecg: NodeCG) => {
            new YourServiceNameService(nodecg, "your-service-name", __dirname, "../your-service-name-schema.json").register();
        };
        ```
        ````

    === "Output"

        ```typescript
        import { NodeCG } from "nodecg-types/types/server";
        module.exports = (nodecg: NodeCG) => {
            new YourServiceNameService(nodecg, "your-service-name", __dirname, "../your-service-name-schema.json").register();
        };
        ```

## [`pymdownx.inlinehilite`](https://facelessuser.github.io/pymdown-extensions/extensions/inlinehilite/)

!!! EXAMPLE "Inline Highlighted Code Example"

    === "Markdown"

        ```markdown
        `` Here is some code: `#!py3 import pymdownx; pymdownx__version__`.

        The mock shebang will be treated like text here: ` #!js vartest = 0; `. ``
        ```

    === "Output"

        Here is some code: `#!py3 import pymdownx; pymdownx.__version__`

        The mock shebang will be treated like text here: ` #!js var test = 0; `.

## [`pymdownx.superfences`](https://facelessuser.github.io/pymdown-extensions/extensions/superfences/)

1.  Allowing the nesting of fences under blockquotes, lists, or other block
    elements.
2.  Ability to specify custom fences to provide features like flowcharts,
    sequence diagrams, or other custom blocks.
3.  Allow disabling of indented code blocks in favour of only using the fenced
    variant (off by default).
4.  Experimental feature that preserves tabs within a code block instead of
    converting them to spaces which is Python Markdown's default behaviour.

## [`pymdownx.tabbed`](https://facelessuser.github.io/pymdown-extensions/extensions/tabbed/)

!!! EXAMPLE "Example Tabs"

    === "Markdown"

        ```markdown
        === "Tab 1"

            Markdown **content**.

            Multiple paragraphs.

        === "Tab 2"

            More Markdown **content**.

            - list item a
            - list item b
        ```

    === "Output"

        === "Tab 1"

            Markdown **content**.

            Multiple paragraphs.

        === "Tab 2"

            More Markdown **content**.

            - list item a
            - list item b

## [`pymdownx.tasklist`](https://facelessuser.github.io/pymdown-extensions/extensions/tasklist/)

GFM style task lists

!!! EXAMPLE "Task lists"

    === "Markdown"

        ```markdown
        - [X] item 1
          * [X] item A
            * [ ] item B
                more text
                + [x] item a
                + [ ] item b
                + [x] item c
            * [X] item C
        - [ ] item 2
        - [ ] item 3
        ```

    === "Output"

        - [X] item 1
          * [X] item A
            * [ ] item B
                more text
                + [x] item a
                + [ ] item b
                + [x] item c
            * [X] item C
        - [ ] item 2
        - [ ] item 3

## [`admonition`](https://python-markdown.github.io/extensions/admonition/)

> Possible types are:  
> NOTE, SUMMARY, ABSTRACT, TLDR, INFO, TODO, TIP, HINT, SUCCESS, CHECK, DONE,
> QUESTION, HELP, FAQ, WARNING, ATTENTION, CAUTION, FAILURE, FAIL, MISSING,
> DANGER, ERROR, BUG, EXAMPLE, SNIPPET, QUOTE, CITE

!!! EXAMPLE "Inline Highlighted Code Example"

    === "Markdown"

        ```markdown
        !!! HINT "optional explicit title within double quotes"

            Any number of other indented markdown elements.

            This is the second paragraph.
        ```

    === "Output"

        !!! HINT "optional explicit title within double quotes"

            Any number of other indented markdown elements.

            This is the second paragraph.
