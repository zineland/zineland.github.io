Every markdown file located in `pages` will be rendered as a **Page**. Just intuitive like this:

```
$ tree pages
pages
├── about.md        # will be rendered as https://your-domain.com/about
├── blog            
│   └── first.md    # will be rendered as https://your-domain.com/blog/first
├── blog.md         # will be rendered as https://your-domain.com/blog
└── faq.md          # will be rendered as https://your-domain.com/faq

1 directory, 4 files
```