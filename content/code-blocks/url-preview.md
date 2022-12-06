
The `urlpreview` code block helps you render OPG preview info of an URL in the markdown article. 

## Syntax

The syntax is:

~~~markdown
```urlpreview [, image: true|false]
https://github.com
```
~~~

### Config

| Config name | Type   | Explanation |
| ----------- | ------ |------ |
| image       | boolean | whether you need to render the preview image (default: true) |

#### image: true

~~~
```urlpreview
https://github.com
```
~~~

```urlpreview
https://github.com
```

#### image: false
~~~
```urlpreview, image: false
https://github.com
```
~~~

```urlpreview, image: false
https://github.com
```

## zine-data.json

To cache every preview URL, Zine will generate a file called `zine-data.json` to store all preview info. You should add this file to your version control system.

```json
{
  "urlPreviews": {
    "https://github.com": [
      "GitHub: Let’s build from here · GitHub",
      "GitHub is where over 94 million developers shape the future of software, together. Contribute to the open source community, manage your Git repositories, review code like a pro, track bugs and feature",
      "https://github.githubassets.com/images/modules/site/social-cards/campaign-social.png"
    ]
  }
}
```

> However, it's possible to add more fields to `zine-data.json` in the future.

You can use `zine lint` command to lint the `zine-data.json`, such as checking the broken links, redirection links, etc.