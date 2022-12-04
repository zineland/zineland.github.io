The callout block can help you highlight some content.

## Syntax

The syntax is:

~~~markdown
```callout[, theme, bg_color, border_color]
Callout content
```
~~~

## Config

| Config name | Type   | Explanation |
| ----------- | ------ |------ |
| theme       | enum | the theme |
| bg_color      | color | the background color |
| broder_color  | color | the border color |

For example:
~~~
```callout, bg_color:#faf8f3, border_color:#ececec
Zine is a static site generator for magazine.
```
~~~

will render to:

```callout, bg_color:#faf8f3, border_color:#ececec
Zine is a static site generator for magazine.
```

However, zine provice some builtin themes.

## Callout theme

### grey

```callout, theme:grey
Grey callout

The syntax is: `callout, theme: grey`

```

### orange

```callout, theme:orange
Orange callout

The syntax is: `callout, theme: orange`
```

### red

```callout, theme:red
Red callout

The syntax is: `callout, theme: red`
```

### yellow

```callout, theme:yellow
Yellow callout

The syntax is: `callout, theme: yellow`
```

### green

```callout, theme:green
Green callout

The syntax is: `callout, theme: green`
```

### blue

```callout, theme:blue
Blue callout

The syntax is: `callout, theme: blue`
```

### purple

```callout, theme:purple
Purple callout

The syntax is: `callout, theme: purple`
```