# What is this.

This is the theme for Hugo that supports the [Accelerated Mobile Pages Project](https://www.ampproject.org/).

[Hugo :: A fast and modern static website engine](https://gohugo.io/)

## PC View

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/screenshot.png)

## SP View(Responsive)

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/responsive.png)

## Article footer

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/taxonomy.png)

## AMP supported

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/amp-valid.png)

# Features

* [Accelerated Mobile Pages Project](https://www.ampproject.org/) a.k.a AMP supported
* Responsive design
* Google Analytics
* Thumbnail
* High score by Google Page Speed Insight.
* Share button
* Structured data(Article and Breadcrumb)
* Twitter cards
* OGP
* Specializing in SEO

# `config.toml` example

```
baseurl = "https://example.com/"
title = "SiteTitle"

googleAnalytics = "UA-XXXXXXXX-XX" # Optional

[params]
  contact = "contact@example.com" # Optional
  dateformat = "Jan 2, 2006" # Optional
  # Fonts settings.
  googlefonts = "https://fonts.googleapis.com/css?family=Lobster|Lato:400,700" # Optional, Include google fonts.
  fontfamily = "Lato,YuGothic,'Hiragino Kaku Gothic Pro',Meiryo,sans-serif" # Optional, Override body font family.
  logofontfamily = "Lobster, cursive" # Optional, Override logo font.
```

# Frontmatter example

```
+++
date = "2016-09-28T17:00:00+09:00"
title = "Article title here"
thumbnail = "images/thumbnail.jpg" # Optional, referenced at `$HUGO_ROOT/static/images/thumbnail.jpg`
+++
```

# Recommended directory structure

This themes `Header Menu` is using `Section`.
Recommend that you use the section than taxonomy.

```
.
├── config.toml
├── content
│   ├── section1         # Separated by Section.
│   │   └── article1.md
│   └── section2
│       └── article2.md
├── layouts
└── static
    ├── favicon.ico
    └── images           # Place here thumbnail images.
        └── thumbnail.png
```

# Shortcodes

## Iframe

```
{{% iframe src="https://www.youtube.com/embed/XXXXXXX" w="560" h="315" %}}
```

## Image

```
{{% img src="images/image.jpg" w="600" h="400" %}}
{{% img src="images/image.jpg" w="600" h="400" class="right" %}}
{{% img src="images/image.jpg" w="600" h="400" class="left" %}}
{{% img src="images/image.jpg" w="600" h="400" caption="Referenced from wikipedia." href="https://en.wikipedia.org/wiki/Lorem_ipsum" %}}
```

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/include-images.png)

## Clear

Break float.

```
{{% img src="images/image.jpg" w="600" h="400" class="right" %}}

brabrabra # Displayed left of the image.

{{% clear %}}

brabrabra # Displayed below of the image.
```

## Twitter

```
{{% twitter tweetid="780599416621297xxx" %}}
```

# Development mode

Supported development mode.

```
env HUGO_ENV="DEV" hugo server --watch --buildDrafts=true --buildFuture=true -t solit
```

This mode is

* Not show Google Analytics tags.
* Show `IsDraft`.
* Show `WordCount`.

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/development-mode.png)

And set `{{ if ne (getenv "HUGO_ENV") "DEV" }} Set elements here. {{ end }}` if you want to place only in a production environment.

# Inspired by

* [LinkedIn Redesign ~ Freebies Vol\.4 on Behance](https://www.behance.net/gallery/42205705/LinkedIn-Redesign-Freebies-Vol4)

# Using iconset

* [Iconset:watchify\-v1\-0\-80px icons \- Download 25 free & premium icons on Iconfinder](https://www.iconfinder.com/iconsets/watchify-v1-0-80px)

# Colorscheme

* [Material Design Colors, Material Colors, Color Palette \| Material UI](https://www.materialui.co/colors)

