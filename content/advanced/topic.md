Each article can specify one or more topics, like this:

```toml
[[article]]
file = "topic.md"
title = "Article topic"
author = "zine-team"
topic = ["advanced", "tutorial"]
pub_date = "2022-12-16"
```

However, each topic should been declared in the root `zine.toml`:

```toml
[topics]
advanced = { name = "Advanced knowledge", description = "Advanced feature of zine" }
# all of fields are optional
tutorial = {}
```

Zine will generate a dedicated topic page for each topic, for example:

```
https://example.com/topic/advanced
https://example.com/topic/tutorial
```

Also, the user can check all topics in [/topics](/topics) page.