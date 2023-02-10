Here is the directory structure of a regular zine project.

```

├── content                     # the convention directory of markdown fiels of zine project 
│   ├── issue-1                 # the directory of an issue
│   │   ├── article.md
│   │   └── zine.toml           # the zine.toml of issue-1
│   └── issue-2                 # the directory of another issue
│       ├── another-article.md
│       └── zine.toml           # the zine.toml of issue-2
├── locales                     # the optional localization directory
├── static                      # the convention directory of static files, such as image, css, etc
│   ├── xx.jpeg
│   └── theme.css
└── zine.toml                   # the root zine.toml of zine porject
```

> Please check the `/advanced/l10n` page for more detail about the `locales` directory.

A Zine project mainly consists of two kinds `zine.toml` files and a bunch of markdown files.

## Root zine.toml

This root `zine.toml` file describes your site meta and all your issue's info.

```toml
[site]
url = "https://your-domain.com"
name = "Your Zine Site Name"
description = ""
# the OpenGraph social image path. (optional)
social_image = "/path/to/social_image"
# the repository edit url (optional)
edit_url = "https://github.com/zineland/zine/edit/master/demo"
# the locale to localize your Zine site. default to "en".
# Zine has builtin supported locales, please check the `locales` directory of zine's repo.
locale = "en"
# the menu tabs (optional)
menu = [
    { name = "About", url = "/about" },
    { name = "Blog", url = "/blog" },
]

# Declare authors of this magazine.
[authors]
# set editor to true will show the Editor badge on the author profile page
zine_team = { name = "Zine Team", avatar = "/path/to/avatar/", editor = true, bio = "The Zine Team." }
# all fields are optional.
foo = {}

# Declare topics of this magazine.
[topics]
topic1 = { name = "Topic 1", description = "" }
topic2 = {}

# You can customize some theme elements in this section.
# All of those elements are optional.
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

# You can customize some markdown styles in this section.
# All of those elements are optional.
[markdown]
# enable the code highlighting. default is true
highlight_code = true
# custom highligh theme
highlight_theme = "ayu-light"
```

For more about theme customization, please check the `/customization/theme` page.

## Issue zine.toml

The issue `zine.toml` file list all articles contained within a given issue.

```toml
# the number of this issue
number = 1
# issue title
title = "Issue 1"
# the slug of this issue, will be the directory name if this field is missing
slug = "issue"

[[article]]
# the slug of this article. E.g: https://your-domain.com/s1/1
# optional. Fallback to `file` name if missing.
slug = "1"
# the markdown file path of this article
file = "1-first.md"
# the title of this article
title = "First article"
# the optional author id of this article.
# also support multiple co-authors:
# author = ["author1", "author2"]
author = "zine-team"
# the optional topic of this article.
topic = ["topic1", "topic2"]
# the cover of this article
cover = ""
# the publish date of this article
pub_date = "2022-03-20"
# whether to publish this article or not
publish = true
# whether mark this article as a featured article. 
# the featured articles will be shown on the home page
featured = true
# When articles are reposted from the original source, set a
# canonical property to help prevent duplicate content issues for search engines.
canonical = "URL of the orginal Article"
# the translations of this artcle.
# the key of syntax is `i18n.[locale]`, the value is the article object.
i18n.fr = { file = "1-first-fr.md", title = "Premier article", pub_date = "2022-11-27" }
i18n.zh = { file = "1-first-zh.md", title = "第一篇文章", pub_date = "2022-11-27" }

# Another article
[[article]]
```
