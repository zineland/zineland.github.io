Zine provides a neat way to link to another article within the same magazine.

## Syntax

The syntax is also simple, just specify the article path, such as `/{issue_slug}/{article_slug}` or `/{article_path}` (if the article has set a *path*). If the path is invalid, the article link wouldn't render, instead, render the raw text.

## Example

Since the path of [Getting Started - Overview](/getting-started/overview) page is **/getting-started/overview**, we can use \`/getting-started/overview\` to render the `/getting-started/overview` page link.

Here the **getting-started** and **overview** are the slug of issue and article respectively.

If an article has set a path:

```toml
[[article]]
file = "example.md"
path = "/example"
```

We can use \`/example\` to render the article link.