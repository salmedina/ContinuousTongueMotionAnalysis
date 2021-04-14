
# README

This project is based on Gravity and has been adapted to be used for publishing static sites for academic projects with a paper feel and look.


# INSTALLATION

### Dependencies

Gravity uses Jekyll and it's built-in SCSS compiler for the associated CSS, so the first thing you'll need is Jekyll itself:

```bash
$ gem install jekyll
```

In case you don't have the `bundler` gem installed already, you can install it as follows:

```bash
$ gem install bundler
```

For pagination, Gravity uses the [jekyll-paginate](https://jekyllrb.com/docs/pagination/) gem :

```bash
$ gem install jekyll-paginate
```

***

# USAGE

Once you have the required gems, you can go ahead and clone the
[Gravity repository](https://github.com/hemangsk/Gravity) or [download](https://github.com/hemangsk/Gravity/archive/master.zip)
a zip of the master branch.

Run :

```bash
$ jekyll serve
```

Jekyll should now be generating your content!

***

# CREATE PAGES

- Create a .md file in the root directory.
- Name the file with the desired page link name.
  `abstract.md`
  `results.md`
- Write the *Front Matter* and content in the file.

### FORMAT

```
---
layout: page
title: Phones
permalink: /phones/
category: "phones"
tagline: "Analysis"
---
```

***

#### DIRECTORY STRUCTURE

```
├── css                                         # => Output of the combined SASS files
│   └── style.scss
├── _includes                                   # => Contains partials that can be used with your layouts
│   ├── footer.html
│   ├── header.html
│   ├── head.html
│   ├── icon-github.html
│   ├── icon-github.svg
│   ├── icon-twitter.html
│   └── icon-twitter.svg
├── _layouts                                    # => Layout related HTML files
│   ├── archive.html
│   ├── default.html
│   ├── page.html
│   └── post.html
└── _sass                                       # => SASS partials for styling
|   ├── _base.scss
|   ├── _layout.scss
|   └── _syntax-highlighting.scss
├── _config.yml                                 # => Configuration options or flags for your site go here
├── abstract.md
├── results.md
├── feed.xml
├── index.html
├── LICENSE.txt                                 # => Licensing information
├── README.md
```
