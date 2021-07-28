# markdown-it-container-question

## What is this?

VSCode extension that allows parsing of the following syntax in Markdown:

```
::: q What's your question?
this is hidden, collapsable content.
:::
```

and produces the infamous HTML snippet often used in Markdown:

```html
<details>
<summary>What's your question?</summary>
...this is hidden, collapsable content...
</details>
```

Check how `<details><summary>...` snippet behaves in action:
<details>
<summary>What's your question?</summary>
this is hidden, collapsable content.
</details>

## Features

`question` and `answer` are names of CSS classes assigned to HTML elements. Use your own `style.css` to make questions and answer prettier.

Add style for markdown in VSCode JSON settings:

```
"markdown.styles": ["./relativepath/to/style.css"]
```

E.g. of `style.css`
```
.answer {
  margin: 1em 0em 0em 3em;
  padding-left: 1em;
  border-left: 3px solid rgba(0, 0, 0, 0.2);
  display: block;
}
.question {
  color: red;
}
```
