Markdown Viewer
---------------
d-markdown-app
13742.x

May 2023 

# Purpose
Opens and parses a markdown file using another file as the index of the headers. This enables a 2 column "help" app to be delivered. Each group indexed by header is opened and closed depending on the menu index selected. 

# Markdown
Based on [Sitemark](https://plugnburn.github.io/sitemark/); 
Markdown syntax used resembles both classical and GitHub-flavored Markdown versions, however it does not support some advanced features such as tables or reference-style links. Supported tags are:

- Headings, single-line form: `# Heading level 1`, `## Heading level 2` and so on
- Headings of levels 1 and 2, two-line form:
    ```
    Heading level 1
    ===============
    
    Heading level 2
    ---------------
    ```
- Inline formatting: `**bold**` or `__bold__`, `*italic*` or `_italic_`, `~~strike~~`, `:"quote":` and even non-standard `___underline___` (triple underscore) tag!
- Preformatted inline blocks:`` `inline code` ``
- Preformatted multiline blocks:
```
    ```
    first line of preformatted text
    second line of preformatted text
    etc...
    ```
```
- Block quotes:
```
    > first line of quote
    > second line of quote
    > etc...
```
- Lists:
```
    - unordered item 1
    - unordered item 2
    
    * another unordered item 1
    * another unordered item 2
    * another unordered item 3
    
    1. ordered item 1
    2. ordered item 2
    3. ordered item 3
    4. ordered item 4
``` 
- Links: `[link text](http://example.com)`
- Images: `![alt text](http://example.com/flower.jpg)`
- Horizontal rules: `****************` (5 and more asterisks on a new line)
- Paragraphs: just like in standard Markdown, any non-special text is enclosed into paragraphs by default, just surround it with newlines.
 
HTML in Markdown documents will pass as is, unless enclosed into inline or multiline preformatted blocks, in which case it will be escaped appropriately.

For grouping and wrapping text into a Div container, we also use this {id}[text] where the id maps to the Index.

# Setup
2 files needed. The markdown and the menus. The raw id of the menus is used by the js to find the id in the markdown with a "t" appended e.g menu id=welcome and markdown id=twelcome. 

# Development 
open -n -a /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --args --user-data-dir="users/shared" --disable-web-security
runs without cors for local installation

# References
[](https://javascript.plainenglish.io/simple-markdown-parser-with-javascript-and-regular-expressions-f0c8d53449a4) 
[](https://www.markdownguide.org/basic-syntax/) 