## Config

You can customize some theme elements in this `[theme]` section of root `zine.toml`. All of those elements are optional:

```toml
[theme]
# the primary color
primary_color = "#abcdef"
secondary_color = "#fff"
# the main text color
main_color = "#000"
# the link color in article content
link_color = "#e07312"
# the background image
background_image = "/static/background.png"
# you can customize your head here, such as your css, js
head_template = "templates/head.html"
# you can customize your footer here
footer_template = "templates/footer.html"
# you can extend the article page, for example adding comment widget
article_extend_template = "templates/article-extend.html"
```

Here is an example of theme customization:

![](/static/theme.png)

However, those color fields aren’t enough for customization, in order to advanced customization, you should override the built-in CSS style. See `/customization/css` page.

## Templates

Zine has an opinionated layout and CSS style, you can extend those layouts and styles via those `template` fields. All those templates support **Jinja2** syntax.

### Head

Customize `head_template` to provide your own custom fonts, Javascript, and CSS links.

For example, here is the custom head template of this website.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css?family=Alfa+Slab+One&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Fira+Sans:ital,wght@0,400;0,500;0,600;1,400;1,500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="/static/theme.css">
```

### Footer

The default footer of zine is boring. You can customize your footer via `footer_template`.

### Article

Do you wanna add a comment widget below each article? Easy. Just set an `article_extend_template`.

Take [https://rustmagazine.org](https://rustmagazine.org) as the instance.

```html
<div class="mx-4">
  <div class="giscus"></div>
</div>
<script
  src="https://giscus.app/client.js"
  data-repo="rustmagazine/rustmagazine"
  data-repo-id="R_kgDOIcB-NQ"
  data-category="Articles"
  data-category-id="DIC_kwDOIcB-Nc4CSkor"
  data-mapping="pathname"
  data-strict="0"
  data-reactions-enabled="1"
  data-emit-metadata="0"
  data-input-position="top"
  data-theme="light"
  data-lang="en"
  data-loading="lazy"
  crossorigin="anonymous"
  async>
</script>
```

![](/static/article-widget.png)

## Code highlight

You can customize some markdown styles in this section. All of those elements are optional.

```toml
[markdown]
# enable the code highlighting. default is true
highlight_code = true
# custom highligh theme
highlight_theme = "ayu-light"
```

You can visit the theme directory of zine to check all of highlighting themes.

```urlpreview
https://github.com/zineland/zine/tree/master/sublime/themes
```