
The author code is designed to render the avatar-name link on the markdown page.

## Syntax

The syntax is very simple, just write like this \`@author_id\`.
If the `author_id` is declared in the `[authors]` table of the root `zine.toml`, 
it will render the UI as expected, otherwise it fallback into the raw code UI.

```toml
[authors]
zine-team = { name ="Zine Team" }
```

## Example

For example, \`@zine-team\` will be rendered to `@zine-team`, while \`@robot\` will not be rendered (because isn't declared in the `[authors]` section).
