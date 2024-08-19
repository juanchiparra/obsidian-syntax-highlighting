
You can contribute by updating existing snippets or creating new ones.

- To update: Follow the current structure of the snippet you want to update and add/modify what you consider an improvement
- To create: Use the template available [here](src/template.css).

In both cases, send a pull request with your changes for review.

Snippets use the [CSS variables](https://docs.obsidian.md/Reference/CSS+variables/Editor/Code) defined by Obsidian.

```css
body {
    --code-background: color;
	--code-white-space: pre-wrap;
    --code-size: 13px;
    --code-normal: color;
    --code-comment: color;
    --code-function: color;
    --code-important: color;
    --code-keyword: color;
    --code-operator: color;
    --code-property: color;
    --code-punctuation: color;
    --code-string: color;
    --code-tag: color;
    --code-value: color;
}
```

You can also configure the appearance of elements that have specific classes.

⚠️**Important!** Obsidian uses two different libraries to modify syntax highlighting. One for the edit view and one for the read view, so there might be some inconsistency between them.

For each case, you would have to use the following structure.

```css
.markdown-preview-view {.class}, /*Reading view*/
.cm-s-obsidian span{.class} /*Editing view*/ {
    color: --code-operator;
}
```

This is the default way Obsidian customizes syntax highlighting.

```css
/* Reading view */
.token.comment,
.token.prolog,
.token.doctype,
.token.cdata {
    color: var(--code-comment);
}
.token.tag,
.token.constant,
.token.symbol,
.token.deleted {
    color: var(--code-tag);
}

.token.punctuation {
    color: var(--code-punctuation);
}

.token.boolean,
.token.number {
    color: var(--code-value);
}

.token.selector,
.token.attr-name,
.token.string,
.token.char,
.token.inserted {
    color: var(--code-string);
}

.token.operator {
    color: var(--code-operator);
}

.token.entity,
.token.parameter,
.token.property,
.token.url,
.language-css .token.string,
.style .token.string,
.token.variable {
    color: var(--code-property);
}

.token.atrule,
.token.attr-value,
.token.builtin,
.token.function,
.token.class-name,
.token.property-access {
    color: var(--code-function);
}

.token.keyword {
    color: var(--code-keyword);
}

.token.regex,
.token.important {
    color: var(--code-important);
}

/* Editing view */
.cm-inline-code,
.cm-math {
    color: var(--code-normal);
}

.cm-comment,
.cm-meta {
    color: var(--code-comment);
}

.cm-tag {
    color: var(--code-tag);
}

.cm-punctuation,
.cm-bracket,
.cm-hr {
    color: var(--code-punctuation);
}

.cm-number {
    color: var(--code-value);
}

.cm-qualifier,
.cm-string,
.cm-string-2 {
    color: var(--code-string);
}

.cm-operator {
    color: var(--code-operator);
}

.cm-link,
.cm-variable,
.cm-variable-2,
.cm-variable-3 {
    color: var(--code-property);
}

.cm-builtin,
.cm-property,
.cm-attribute,
.cm-type {
    color: var(--code-function);
}

.cm-keyword {
    color: var(--code-keyword);
}
```

If you want to know more about how to configure the style in Obsidian, I recommend you read [Getting comfortable with Obsidian CSS](https://forum.obsidian.md/t/getting-comfortable-with-obsidian-css/133) and [How to style Obsidian](https://publish.obsidian.md/hub/04+-+Guides%2C+Workflows%2C+%26+Courses/Guides/How+to+Style+Obsidian).

Thank you for wanting to contribute!
