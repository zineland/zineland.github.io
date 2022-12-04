The `quote` is a handy block to help you quote sentence, paragraph.

## Syntax

~~~toml
```quote
author = ""
bio = ""
content = ""
```
~~~

## Config

| Config name | Type   | Explanation |
| ----------- | ------ |------ |
| author       | string | the author name (optional) |
| bio        | string | the bio of author (optional) |
| content    | string | the content |

The content `bio` and `content` can be markdown format. Actually, the content of `quote` is [toml](https://toml.io) format, therefore you can use multiple lines. For example:

~~~toml
```quote
author = "Zine Team"
content = """
The [zine documentation](/) website is built by [zine](https://github.com/zineland/zine) itself.

![](/static/zine.png)
"""
```
~~~

```quote
author = "Zine Team"
content = """
The [zine documentation](/) website is built by [zine](https://github.com/zineland/zine) itself.

![](/static/zine.png)
"""
```