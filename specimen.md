###### THE DOCUMENTARY RECORD • VOLUME I

# Renegotiating our Relationships with Technology

*Why we need to renegotiate our relationships with ourselves, our communities and the ways in which we use technology*

###### BY CHRISTOPHER STEEL • JUNE 27, 2026

---

For a generation now, technology has been designed to capture and manipulate our attention rather than to serve us in our endeavours. The tools we use daily were not built to extend our capabilities but to harvest them, optimising for engagement metrics that have nothing to do with the lives of the people on the other side of the screen.

> The most powerful technology is the kind that disappears into the work, leaving the individuals who employ it more capable and able to accomplish their goals.

## What Agency Actually Looks Like

Reclaiming agency does not mean rejecting technology. It means insisting that the tools we use answer to us rather than primarily to the interests of the platforms that provide them. It means choosing to build software that can be understood, modified, and owned, and resisting the gradual replacement of skill with dependency.

---

## Theme Test: Headings

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

---

## Theme Test: Body Text

This is a standard paragraph using EB Garamond at 19px. The line-height is 1.75, and paragraphs have a bottom margin of 26px. The body colour is #222 on a parchment card (#faf8f3), which sits on the warm page background (#f0ece4). The contrast is clean and the measure feels comfortable at 820px.

**Bold text** sits inside a paragraph. *Italic text* also sits inside a paragraph. **Bold and *bold italic* together** work within the same run. `Inline code` appears within prose. A [link to a source](https://universalcake.ca) uses the inline link style.

---

## Theme Test: Lists

Unordered list:

- First item in the list
- Second item in the list
- Third item, which is a bit longer to test line-height and wrapping behaviour across multiple lines of text in the list

Ordered list:

1. First ordered item
2. Second ordered item
3. Third ordered item, again a bit longer to see how the numeral hangs relative to the wrapped text below it

Nested list:

- Parent item
    - Nested child item
    - Another nested child item
- Back to parent level

Task list:

- [x] Completed task
- [ ] Incomplete task
- [ ] Another incomplete task

---

## Theme Test: Blockquotes

Single-level blockquote:

> Typography is what language looks like. In the digital age, it has become the voice of our visual culture.

Longer blockquote with multiple sentences:

> Good typography is invisible. It does its work quietly, shaping the reader's experience without calling attention to itself. When it fails, however, every reader notices, even if they cannot name what has gone wrong.

---

## Theme Test: Code

Inline code: `font-family: "Cinzel", serif`

Fenced code block:

```css
h1 {
    font-family: "Cinzel", serif;
    font-weight: 600;
    font-size: 48px;
    line-height: 1.15;
    letter-spacing: .02em;
    margin: 0 0 16px 0;
}
```

```javascript
function applyTheme(selector, tokens) {
    const el = document.querySelector(selector);
    Object.entries(tokens).forEach(([key, value]) => {
        el.style.setProperty(`--${key}`, value);
    });
}
```

```python
def load_theme(path: str) -> dict:
    with open(path, "r") as f:
        return json.load(f)
```

```bash
cp folio.css ~/.config/Typora/themes/
cp -R folio ~/.config/Typora/themes/
```

---

## Theme Test: Tables

| Element | Font | Size | Weight |
|---------|------|------|--------|
| Body | EB Garamond | 19px | 400 |
| H1 | Cinzel | 48px | 600 |
| H2 | Cinzel | 22px | 600 |
| H3 | Cinzel | 15px | 400 |
| Blockquote | EB Garamond | 26px | 400 italic |
| Meta / H5 | Cinzel | 11px | 400 |
| Byline / H6 | Cinzel | 11px | 400 |

---

## Theme Test: Definition List

Cinzel
: A typeface by Natanael Gama based directly on Roman inscriptional letterforms, particularly those of Trajan's Column. Suited to display and titling use. Licensed under SIL OFL 1.1.

EB Garamond
: A revival of Claude Garamond's sixteenth-century type by Georg Duffner and Octavio Pardo. Suited to body text and extended reading. Licensed under SIL OFL 1.1.

---

## Theme Test: Horizontal Rule

Before the rule.

---

After the rule.

---

## Theme Test: Footnotes

Typography has been called the invisible art.[^1] When it works well, readers do not notice it. When it fails, they notice immediately, even if they cannot articulate why.[^2]

[^1]: A phrase attributed to various typographers across the twentieth century.
[^2]: Discussed at length in Robert Bringhurst, *The Elements of Typographic Style*, Hartley and Marks, 1992.

---

## Theme Test: Emphasis Variants

Plain text for reference. **Bold text.** *Italic text.* ***Bold italic text.*** ~~Strikethrough text.~~ `Inline code.`

---

## Theme Test: Mermaid Diagrams

Flowchart:

```mermaid
flowchart TD
    A[Source Markdown] --> B[Typora Renderer]
    B --> C{Theme Applied?}
    C -->|Yes| D[Styled Output]
    C -->|No| E[Default Style]
    D --> F[Export HTML / PDF]
    E --> F
```

Sequence diagram:

```mermaid
sequenceDiagram
    participant Author
    participant Typora
    participant Theme
    Author->>Typora: Open markdown file
    Typora->>Theme: Load folio.css
    Theme-->>Typora: Apply fonts and layout
    Typora-->>Author: Render styled document
```

Gantt chart:

```mermaid
gantt
    title Folio Theme Development
    dateFormat  YYYY-MM-DD
    section Design
    Mockup review       :done, 2026-06-24, 2026-06-25
    Token extraction    :done, 2026-06-25, 2026-06-26
    section Build
    CSS authoring       :done, 2026-06-26, 2026-06-27
    Font bundling       :done, 2026-06-27, 2026-06-27
    section Test
    Visual QA           :active, 2026-06-27, 2026-07-04
    Refinements         : 2026-07-04, 2026-07-14
```

Pie chart:

```mermaid
pie title Font Usage in Folio
    "EB Garamond (body, blockquote)" : 65
    "Cinzel (headings, labels)" : 35
```

---

## Theme Test: Images

![A placeholder image representing editorial layout](https://via.placeholder.com/820x400?text=Folio+Image+Test)

*Caption text sits below the image in italic body type.*

---

## Theme Test: Math

Inline math: $E = mc^2$

Block math:

$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$
