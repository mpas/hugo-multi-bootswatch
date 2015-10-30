## Changes

This is a list of changes and improvements over original [hugo-multi-bootswatch](https://github.com/mpas/hugo-multi-bootswatch) theme.

### Support for lang meta in HTML

Original theme uses ```<html lang='en-US'>``` and ```<body lang='en'>``` without easy way to change this. In this theme you can change this parameter by adding ```languageCode = 'your_language_code'``` in your ```[params]``` section of _config.toml_.

### Nicer title for tab in your browser

Instead of priting just post's title (as in original theme) I decided to print site main title after post's one.

### Summary instead of Content on frontpages

Because it's looking nice. Don't forget to paste ```<!--more-->``` in your content!

### Avoiding Summary for short posts

If you want some (probably, short) post displayed without cut on frontpages, use variable ```nocut = true``` in post's front matter.

### Separate copyright string

Define ```copyright = 'blah'``` in ```[params]``` section of _config.toml_.

### Dynamic links on navbar

After default _Home_ and _Blog_ link there will be no default _Resume_ and _About_ link. Links to all posts with `menu = 'main'` will be placed instead.

# Basic localization

You can define custom names of many elements inside template. This section on _config.toml_ is self-descriptive:

```
# all this is optional
[params.strings]
  home_navbar_link = "Home"
  blog_navbar_link = "Blog"
  read_more_link = "Read more"
  posts_list_header = "Posts"
  date_format = '02.01.2006'
```
