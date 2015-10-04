Hugo Bootswatch Theme
==================

Hugo BootSwatch Theme is a single column theme for [hugo](http://hugo.spf13.com/) based on [Twitter Bootstrap](http://getbootstrap.com/) and a css styling from [Bootswatch](http://bootswatch.com/).

It is a simple template containing a nice header menu bar and content area. Default the theme support 2 types of content.

* pages (used for About/Resume pages)
* posts (used for standard blogposts)

---
* [Installation](#installation)
* [Usage](#usage)
* [Configuration](#configuration)
* [Built-in colour themes](#colour-themes)
* [Questions, ideas, bugs, pull requests?](#questions-ideas-bugs-pull-requests)
* [License](#license)
---
## Installation

```
$ cd your_site_repo/
$ mkdir themes
$ cd themes
$ git clone https://github.com/mpas/hugo-bootswatch.git
```

See the [official Hugo themes documentation](http://gohugo.io/themes/installing) for more info.

## Usage

This theme expects a relatively standard Hugo blog/personal site layout:
```
.
└── content
    ├── post
    |   ├── post1.md
    |   └── post2.md
    └── page
        ├── license.md      // this is used in the footer link
        ├── about.md        // used in the header
        └── resume.md       // used in the header
```

Just run `hugo --theme=hugo-bootswatch` to generate your site!

## Configuration

An example of what your site's `config.toml` could look like. All theme-specific parameters are under `[params]` and standard Hugo parameters are used where possible.

```
baseurl     = "http://example.com"  # the baseurl for your website
title       = "Your site title"     # blog title
paginate    = 10                    # the number of posts on a page

[permalinks]
    # Optional. Change the permalink format for the 'post' content type.
    # The format shown here is the same one Jekyll/Octopress uses by default.
    post = "/blog/:year/:month/:day/:title/"

[params]
    # name of the site author; used in header meta information
    author = "<authorname>"

    # social links, used in footer, these must be full URLs.
    twitter = "https://twitter.com/<username>"
    github = "https://github.com/<username>"
    facebook = "https://www.facebook.com/<username>"
    delicious = "https://delicious.com/<username>"

[params.theme]
    inverse = false     # indicating if the theme should use inversed colors
    name = "cerulean"   # name of the theme to use

    # list of possible theme names that can be used
    # name = "cerulean"
    # name = "cosmo"
    # name = "cyborg"
    # name = "default"
    # name = "flatly"
    # name = "journal"
    # name = "lumen"
    # name = "paper"
    # name = "readable"
    # name = "sandstone"
    # name = "simplex"
    # name = "slate"
    # name = "spacelabs"
    # name = "superhero"
    # name = "united"
    # name = "yeti"

```

## Colour themes
All the available color themes from [Bootswatch](http://bootswatch.com/) are available. Please checkout Bootswatch to see what theme you want to use. 

## Screenshots

### Index Page
![index](http://mpas.github.io/hosted/img/hugo-journal/index.png)

### Post Page
![post](http://mpas.github.io/hosted/img/hugo-journal/post.png)

### List Page
![list](http://mpas.github.io/hosted/img/hugo-journal/list.png)

## Questions, ideas, bugs, pull requests?

All feedback is welcome! Head over to the [issue tracker](https://github.com/zyro/hyde-x/issues).

## License

Open sourced under the [MIT license](https://github.com/marcopas/huugo-bootswatch/blob/master/LICENSE).

## License
Open sourced under the MIT license.
