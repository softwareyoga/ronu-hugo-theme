# Ronu Hugo Theme
Ronu is a clean and simple responsive theme for [hugo](https://gohugo.io). It simplicity lies in the fact that there is complete separation of html content and css classes.

Live demo at: [softwareyoga.com](https://www.softwareyoga.com)

No more of messy html like this that is full of css classes...

```html
<html>
<body>
	<div class="w3-row-padding w3-container">
		<div class="w3-col l3 m2">
			<h1>Blog</h1>
		</div>
		<div class="w3-col l6 m8">
			<h2 class="w3-center w3-bold">Post Title</h2>
		</div>  
	</body>
</html>
```

Instead, you will have beautifully formatted plain html without having to specify any css classes, thanks to [Sakura](https://oxal.org/projects/sakura) - A classless css framework.

```html
<html>
	<body>
		<h1>Blog</h1>
		<h2>Post Title></h2>
		<p>Content text</p>
	</body>
</html>
```

The uncluttered user interface (and clean code) makes it a delight to work with, focussing on the most important aspect - The Content.

![Ronu screenshot](https://github.com/softwareyoga/ronu-hugo-theme/blob/master/images/screenshot.png)


## Installation

### Requirements

- Hugo 0.64.1 or higher (extended version because of usage of sass)

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

## Base configuration

First include the following configuration in the config file: 

```toml
# Site settings
baseURL = "https://www.example.com/"
languageCode = "en-us"
title = "MySiteTitle"
theme = "ronu-hugo-theme"
```

## Options

Ronu includes some customizable options, applied via the config file.


### Menu

Create a list of menu item links in the nav bar by assigning "menu.main" in the front matter, like so:

```toml
[[menu.main]]
	name = "Blog"
	url = "/blog/"

[[menu.main]]
	name = "About"
	url = "/about/"
```

### Social
Inform your audience about your social presense in the footer, like so:

```toml
[params]
	authorNname = "Your Name"
	twitterURL = "https://twitter.com/FooBar"
	linkedinURL = "https://www.linkedin.com/in/FooBar"
	email = "foobar@foobar.com"
```

### Main section and siteDescription

By default Ronu assumes the section with most pages as the main section. This is configurable, like so:

```toml
mainSections = ["post"]
```

'siteDescription' is used in the meta info headers in the generated html, configurable as:
```toml
siteDescription = "Your awesome site description"
```

### Theme colours

Ronu ships with many colour schemes based on [Sakura color scheme](https://github.com/oxalorg/sakura/tree/master/scss). To apply a particular colour, change the variables in 'style-in-use.scss'.

Reference values for the built in colour options are specified in the files 'sakura-white.scss', 'sakura-dark.scss', 'sakura-vader.scss' and 'sakura-white.scss' etc.

To create your own theme, look to the file 'style-in-use.scss' and change the provided colors.

![Ronu in dark mode](https://github.com/softwareyoga/ronu-hugo-theme/blob/master/images/screenshot-dark.png)
![Ronu in vader mode](https://github.com/softwareyoga/ronu-hugo-theme/blob/master/images/screenshot-vader.png)

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
