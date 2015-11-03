Hugo Multi Bootswatch Theme
==================

Hugo Multi BootSwatch Theme is a single column theme for [hugo](http://hugo.spf13.com/) based on [Twitter Bootstrap](http://getbootstrap.com/) and a css styling from [Bootswatch](http://bootswatch.com/).

It is a simple template containing a nice header menu bar and content area. Default the theme support 2 types of content.

* posts (used for standard blogposts and optional be placed in the menu!)
* links (used for "linklogs", small blocks of text with link to external site)

You can add posts to the main menu see [Adding posts to main menu](#adding-post-to-main-menu). For understanding, what is "linklog" see [Linklog usage](#linklog-usage)

---

* [Contributors](#contributors)
* [Installation](#installation)
* [Usage](#usage)
* [Adding posts to main menu](#adding-post-to-main-menu)
* [Linklog usage](#linklog-usage)
* [Configuration](#configuration)
* [Built-in colour themes](#colour-themes)
* [Screenshots](#screenshots)
* [Themed screenshots](#themed-screenshots)
    * [Cerulean](#cerulean)
    * [Cosmo](#cosmo)
    * [Cyborg](#cyborg)
    * [Default](#default)
    * [Flatly](#flatly)
    * [Journal](#journal)
    * [Lumen](#lumen)
    * [Paper](#paper)
    * [Readable](#readable)
    * [Sandstone](#sandstone)
    * [Simplex](#simplex)
    * [Slate](#slate)
    * [Spacelab](#spacelab)
    * [Superhero](#superhero)
    * [United](#united)
    * [Yeti](#yeti)

* [Questions, ideas, bugs, pull requests?](#questions-ideas-bugs-pull-requests)
* [License](#license)

---

## Contributors
* [Valdos Sine](http://blog.toofat.ru)
* [Marco Pas](http://mpas.github.io)

---

## Installation

```
$ cd your_site_repo/
$ mkdir themes
$ cd themes
$ git clone https://github.com/mpas/hugo-multi-bootswatch.git
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
```

Just run `hugo --theme=hugo-multi-bootswatch` to generate your site!

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

[author]
    # Optional. Used in RSS feed meta information.
    name = "your name"
    email = "example <at> example <dot> com"

[params]
    # language code for your website
    languagecode = "en-US"

    # name of the site author; used in header meta information
    author = "<authorname>"

    # copyright text; used in footer
    copyright = "2015 ~ <authorname>"

    # social links, used in footer, these must be full URLs.
    twitter     = "https://twitter.com/<username>"
    github      = "https://github.com/<username>"
    facebook    = "https://www.facebook.com/<username>"
    delicious   = "https://delicious.com/<username>"
    linkedin    = "https://www.linkedin.com/in/<username>"
    flickr      = "https://www.flickr.com/photos/<username>"

    # show default summaries on the frontpage or not
    use_summaries = false

# naming of the elements in your blog/site
[params.strings]
    # name of the link to the homepage
    home_navbar_link = "Home"

    # name of the link to the blog page
    blog_navbar_link = "Blog"

    # name of the header used in the post list page
    posts_list_header = "Posts"

    # used date format
    date_format = '02.01.2006'

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

## Adding post to main menu
If you want to add a post to the main menu then include the following to the frontmatter:

    +++
    ...
    menu = "main"
    +++

The `menu = main` will add the post to the menu. These posts will not be included in the listing of normal posts or in the frontpage!!

## Linklog usage

Some people using their blogs as place for sharing links and storing their own opinion on them. In this theme you have separate content type named "link" for this. Every link produces small block of text on your front page (and in RSS feed too) with your comment on it.

For creating new link in your linklog, invoke

```
hugo new link/example.md
```

It will create template with frontmatter like this:

```
+++
draft = true
title = "Title of the external link"
author = "Author of the external content"
ref = "http://example.com/"
type = "link"
+++

Content of your comment on external link goes here.
```

where `title` is a title of your comment on link, `author` is the author of original content you refer to, `ref` is a link to the content, and `type` indicates that this is linklog content. 

## Screenshots
### Index Page
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/index.png)

### Post Page
![post](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/post.png)

### List Page
![list](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/list.png)

## Themed Screenshots
### Cerulean
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/cerulean.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/cerulean.png)

### Cosmo
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/cosmo.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/cosmo.png)

### Cyborg
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/cyborg.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/cyborg.png)

### Default
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/default.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/default.png)

### Flatly
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/flatly.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/flatly.png)

### Journal
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/journal.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/journal.png)

### Lumen
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/lumen.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/lumen.png)

### Paper
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/paper.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/paper.png)

### Readable
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/readable.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/readable.png)

### Sandstone
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/sandstone.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/sandstone.png)

### Simplex
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/simplex.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/simplex.png)

### Slate
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/slate.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/slate.png)

### Spacelab
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/spacelab.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/spacelab.png)

### Superhero
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/superhero.png)
*inversed:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/superhero.png)

### United
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/united.png)
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/united.png)

### Yeti
*normal:*
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_false/yeti.png)
![index](https://raw.githubusercontent.com/mpas/hugo-multi-bootswatch/master/images/inverse_true/yeti.png)


## Questions, ideas, bugs, pull requests?

All feedback is welcome! Head over to the [issue tracker](https://github.com/mpas/hugo-multi-bootswatch/issues).

## License

Open sourced under the [MIT license](https://github.com/mpas/hugo-multi-bootswatch/blob/master/LICENSE.md).
