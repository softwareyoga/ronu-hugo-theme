# Ronu Hugo Theme
Ronu is a clean and simple responsive theme for [hugo](https://gohugo.io). Generates beautifully formatted plain html without using any css classes, thanks to [Sakura](https://oxal.org/projects/sakura) - A classless css framework.

![Ronu screenshot](https://raw.githubusercontent.com/softwareyoga/ronu-hugo-theme/master/images/screenshot.png)

**Live demo** : [softwareyoga.com](https://www.softwareyoga.com)

The uncluttered user interface (and clean code) makes it a delight to work with, focussing on the most important aspect - The Content.

## Features

* Clean html generated with **no** css classes
* Theming support
* Lightning fast load times
* Responsive on all screen sizes
* Automatic dark/light mode based on system preference
* Syntax highlighting
* Pagination 
* SEO Friendly
* Google Analytics support
* RSS feed

## Installation

### Requirements

- Hugo 0.91.2 or higher

### Standard Installation

To install Ronu as your default theme, first clone this repository in the `themes/` directory:

```
    $ git clone https://github.com/softwareyoga/ronu-hugo-theme
```

OR

From the root of your site, execute:

```
git submodule add https://github.com/softwareyoga/ronu-hugo-theme.git themes/ronu-hugo-theme
```

Second, specify `ronu-hugo-theme` as your default theme in the `config.toml` file. Just add the line

```
    theme = "ronu-hugo-theme"
```

at the top of the file.

## Basic configuration

First include the following configuration in the config file: 

```toml
# Site settings
baseURL = "https://www.example.com/"
languageCode = "en-us"
title = "MySiteTitle"
theme = "ronu-hugo-theme"

# By default Hugo assumes the section with most pages as the main section. This is configurable, like so:
[params]
	mainSections = ["post"]
```

## Options

Ronu includes some customizable options, applied via the config file.


### Menu

Create a list of menu item links in the nav bar by assigning "menu.main" in the front matter, like so:

```toml
[[menu.main]]
	name = "Home"
	url = "/"
	weight = 1
	
[[menu.main]]
	name = "Blog"
	url = "/blog/"
	weight = 2
```

### Social
Inform your audience about your social presense in the footer, like so:

```toml
[author]
	name = "Your Name"
	twitterURL = "https://twitter.com/FooBar"
	linkedinURL = "https://www.linkedin.com/in/FooBar"
	email = "foobar@foobar.com"
```

### Site Description
'description' is used in site heading and the meta info headers in the generated html, configurable as:
```toml
[params]
	description = "Your awesome site description"
```

### Theme colours

Ronu supports Automatic dark/light mode based on system preference.
Ronu theming is based on [Sakura color scheme](https://github.com/oxalorg/sakura/tree/master/css).

Files with reference values are available in the above link.
To apply a particular theme, copy the css of your choice into the css directory and include it in the partial `head.html`.

![Ronu in dark mode](https://raw.githubusercontent.com/softwareyoga/ronu-hugo-theme/master/images/screenshot-dark.png)
![Ronu in vader mode](https://raw.githubusercontent.com/softwareyoga/ronu-hugo-theme/master/images/screenshot-vader.png)

## Google Analytics

Google Analytics can be enabled by assigning your tracking code to the `googleAnalytics` variable in the config file:

```toml
googleAnalytics = "Your tracking code"
```

## Author
**Deepak Karanth**
* https://github.com/softwareyoga
* https://www.softwareyoga.com

## Contributing

Contributions are welcome and I will review and consider pull requests.  
Primary goals are:

- Keep it simple. (E.g. Do not add Disqus commenting as readability is the main aspect of this theme, not bells and whistles)
- Keep minimal (or zero) default configuration.
- Avoid interference of content templates with user-defined layouts (css).
- Avoid using JS

## License

Open sourced under the [MIT license](LICENSE.md).
