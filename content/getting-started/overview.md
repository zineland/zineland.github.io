**Zine - a simple and opinionated tool to build your own magazine.**

- Mobile-first.
- Intuitive and elegant magazine design.
- Best reading experiences.
- Theme customizable, extend friendly.
- RSS Feed supported.
- Open Graph Protocol supported.
- I18n and l10n supported.
- Build into a static website, hosting anywhere.

## Static site generator

Zine is essentially a static site generator. The biggest difference of Zine from others (such as Hugo, mdbook) is that Zine is tailored for magazine-like websites. The layout, UI, and structure are opinionated designs. Zine has less flexibility and customizability than other static site generators, while is simpler and more intuitive for the user. Zine is mainly for magazines, while it also can be a good choice for your blog.

## Getting started

Run `zine new your-zine-site`, you'll get following directory:

```
$ tree your-zine-site
your-zine-site
├── content             # The content directory your issues located
│   └── issue-1         # The first issue directory
│       ├── 1-first.md  # The first markdown article in this issue
│       └── zine.toml   # The issue Zine config file
└── zine.toml           # The root Zine config file of this project

2 directories, 3 files
```

Run `zine serve` to preview your zine site on your local computer:

```
$ cd your-zine-site

$ zine serve

███████╗██╗███╗   ██╗███████╗
╚══███╔╝██║████╗  ██║██╔════╝
  ███╔╝ ██║██╔██╗ ██║█████╗  
 ███╔╝  ██║██║╚██╗██║██╔══╝  
███████╗██║██║ ╚████║███████╗
╚══════╝╚═╝╚═╝  ╚═══╝╚══════╝
                             
listening on http://127.0.0.1:3000
```

Run `zine build` to build your zine site into a static website:

```
$ cd your-zine-site

$ zine build
Build success! The build directory is `build`.
```