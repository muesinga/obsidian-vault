//** CSS Text Effects **//

-- CSS Text Overflow --

The CSS `text-overflow` property specifies how overflowed content that is not displayed should be signaled to the user.

It can be clipped, or is can be rendered as an ellipsis (...).

The following example shows how you can display the overflowed content when hovering over the element:

```
div.test:hover {
  overflow: visible;
}
```

-- CSS Word Wrapping --

The CSS `word-wrap` property allows long words to be able to be broken and weap onto the next line.

If a word is too long to fit within an area, it expands outside.

The word-wrap property allows you to force the text to wrap - even if it means splitting it in the middle of a word.

The CSS code is as follows:

```
p {
  word-wrap: break-word;
}
```

-- CSS Word Breaking --

The CSS `word-break` property specifies line breaking rules.

The CSS code is as follows:

```
p.test1 {
  word-break: keep-all;
}

p.test2 {
  word-break: break-all;
}
```

-- CSS Writing Mode --

The CSS `writing-mode` property specifies whether lines of text are laid out horizontally or vertically.

Example of different writing modes:

```
p.test1 {
  writing-mode: horizontal-tb;
}

span.test2 {
  writing-mode: vertical-rl;
}

p.test2 {
  writing-mode: vertical-rl;
}
```

-- CSS Text Effect Properties --

`text-align-last` -- Specifies how to align the last line of a text
`text-justify` -- Specifies how justifies text should be aligned and spaced
`text-overflow` -- Specifies how overflowed content that is not displayed should be signaled to the user
`word-break` -- Specifies line breaking rules for non-CJK scripts
`word-wrap` -- Allows long words to be able to be broken and wrap onto the next line
`writing-mode` -- Specifies whether lines of text are laid out horizontally or vertically

