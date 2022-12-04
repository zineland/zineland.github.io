Most of zine element has a semantic class name, such as `zine-brand`, `zine-menu`, `zine-diamond` and etc. You can override the default styles of those classes.

Here is the customize css file of this website:

```css
.zine-header {
  background-position-x: center;
  background-position-y: top;
  background-size: cover;
}

/* Set font family for those text */
.zine-brand,
.zine-menu,
.zine-diamond,
.zine-button,
.zine-article-title,
.zine-card-title,
h1 {
  font-family: "Alfa Slab One", serif !important;
  color: var(--main-color) !important;
}

.zine-card-date {
  font-family: "Alfa Slab One", serif !important;
}

main {
  font-family: "Fira Sans", Helvetica, Arial, sans-serif;
}

.prose, .max-w-prose {
  max-width: 75ch !important;
}
```

However, don't forgot add your css link into your `head_template`.

```html
<link rel="stylesheet" href="/static/theme.css">
```