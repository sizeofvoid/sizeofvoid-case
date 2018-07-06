# sizeofvoid case - Bootstrap Clone of Hyde for Hugo

sizeofvoid case was built for people who like the original Jekyll theme [Hyde](https://github.com/poole/hyde) and its [port to Hugo](https://github.com/spf13/hyde) but prefer to use [Bootstrap](http://getbootstrap.com).

The theme was built from an empty Bootstrap 3 template with the goal of easy modification for end users. The code is as simple as possible - clearly formatted HTML and a single stylesheet. It's a two column responsive design and currently includes version 3.3.7 of Bootstrap.

Pull requests are welcome.

![sizeofvoid case Screenshot](http://i.imgur.com/i7aarpG.png)


## Contents

- [Installation](#installation)
- [Customization](#customization)
  - [Sidebar](#sidebar)
  - [Color Schemes](#color-schemes)
  - [Analytics](#analytics)
  - [Example Config](#example-config)
- [Author](#author)
- [Inspired By](#inspired-by)
- [License](#license)


## Installation

Installing **sizeofvoid case** is easy. Simple clone this repo to `themes/` in your Hugo folder.

    ~$ cd your-hugo-folder/themes/
    ~$ git clone https://github.com/sizeofvoid/sizeofvoid-case.git

Next, open the `config.toml` file in the base of the Hugo folder and ensure the theme is set to `sizeofvoid-case`.

    theme = "sizeofvoid-case"


## Customization

There are various options you can easily set from your `config.toml` file.

This text will appear after the Title of your site in your `<title>` meta tag:

	description = "A Hugo Theme built with Bootstrap"


### Sidebar

This text will appear in the sidebar immediately under your site's Title:

	sidebarDescription = "A Hugo Theme built with Bootstrap"

This text will appear in a free paragraph below the Title & sidebarDescription and above the menu links. Set it to "" if you don't want it.

	sidebarFreeText = "A optional paragraph of free text. Set to blank in config.toml to clear..."

You can also include useful menu links by including `"menu=main"` items in your `config.toml`. Example:

	[[menu.main]]
		name = "Hugo"
		post = "<span class='glyphicon glyphicon-fire'></span>"
		url = "http://gohugo.io"

You can optionally use the `pre` and `post` vars to include HTML before or after the `name` in the resulting links.


### Color Schemes

In keeping with our attempt to replicate the original Hyde in Bootstrap we've included some colour scheme options. These are not the same as in the original, but we used palettes from the same [Base16](https://github.com/chriskempson/base16) project.

![sizeofvoid case in Light Brown](http://i.imgur.com/oLjV8LV.png)

The themes are:

- Dark Brown (`colorScheme="scheme-darkbrown"`)
- Light Brown (`colorScheme="scheme-lightbrown"`)
- Green (`colorScheme="scheme-green"`)
- Orange (`colorScheme="scheme-orange"`)
- Slate (`colorScheme="scheme-slate"`)

And then a bonus theme that isn't from Base16:

- Gulf Racing (`colorScheme="scheme-gulfracing"`)

Using a theme is as simple as changing the `colorScheme` param in your `config.toml`. Example:

	baseurl = "/blog"
	title = "sizeofvoid case Hugo Theme"

	theme = "sizeofvoid-case"

	[params]
		colorScheme = "scheme-darkbrown"
		DateFormat = "2 Jan 2006"
		description = "A Hugo Theme built with Bootstrap"
		sidebarDescription = "A Hugo Theme built with Bootstrap"
		sidebarFreeText = "A optional paragraph of free text. Set to blank in config.toml to clear..."


#### Creating Your Own Color Scheme

To create your own custom color scheme simply scroll to the end of the `sizeofvoid-case.css` stylesheet in the `your-hugo-dir/themes/sizeofvoid-case/static` folder and edit the template we've left there.

We'll happily accept pull requests for quality color schemes.


### Analytics

This theme supports Hugo's native GA integration & a Piwik integration.

For Google Analytics, simply set your UA number in your `config.toml` file. Example:

	baseurl = "/blog"
	title = "sizeofvoid case Hugo Theme"

	theme = "sizeofvoid-case"

	googleAnalytics = "UA-123-456"

For Piwik, set the following two `params` as below:

	baseurl = "/blog"
	title = "sizeofvoid case Hugo Theme"

	theme = "sizeofvoid-case"

	[params]
		colorScheme = "scheme-darkbrown"
		piwikSiteID = "1234"
		piwikURL = "www.your-site.com"


## Example Config

Here is a full example `config.toml`:

	baseurl = "http://www.your-blog.com"
	title = "Your Blog Title"
	author = "You"
	copyright = "Your Copyright"
	canonifyurls = true
	paginate = 5

	googleAnalytics = ""

	theme = "sizeofvoid-case"

	[params]
		colorScheme = "scheme-darkbrown"
		DateFormat = "2 Jan 2006"
		description = "A blog about content"
		sidebarDescription = "This is my blog about content"
		sidebarFreeText = "A optional paragraph of free text. Set to blank in config.toml to clear..."
		piwikSiteID = ""
		piwikURL = ""

	[[menu.main]]
		name = "Hugo"
		post = "<span class='glyphicon glyphicon-fire'></span>"
		url = "http://gohugo.io"

	[[menu.main]]
		name = "Bootstrap"
		post = "<span class='glyphicon glyphicon-ok'></span>"
		url = "http://getbootstrap.com"


#### sizeofvoid case Uses Bootstrap

**Bootstrap**

 - <http://getbootstrap.com>


## Inspired By

**ExchangeRate-API.com** - the original hugo theme

- <https://github.com/ExchangeRate-API/strange-case>


## Licensing

This theme is released under the [MIT License](LICENSE.md).
