# Visualize

Visualize is a simple, one-page portfolio design with a fully functional lightbox. It is a port of [Visualize](//templated.co/visualize) by [TEMPLATED](//templated.co).

![Hugo Visualize Theme screenshot](https://raw.githubusercontent.com/christianmendoza/hugo-visualize-theme/master/images/screenshot.png)


## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/christianmendoza/hugo-visualize-theme

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.


## Getting started

After installing the Visualize theme successfully it requires a just a few more steps to get your site finally running.


### The config file

Take a look inside the [`exampleSite`](//github.com/christianmendoza/hugo-visualize-theme/tree/master/exampleSite) folder of this theme. You'll find a file called [`config.toml`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/exampleSite/config.toml). To use it, copy the [`config.toml`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/exampleSite/config.toml) in the root folder of your Hugo site. Feel free to customize this theme as you like.


### Example demo

In the [`exampleSite`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/exampleSite) folder you can find an example [`data`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/exampleSite/data) folder with a `gallery.toml` file and [`static`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/static) folder with images. Copy both folders to the root folder of your Hugo site. Start/restart your local server to see an example site with a few test placeholder images.


### Add background image

Name your background image with the filename `bg.jpg` and add it to your `static/images` folder, i.e. `static/images/bg.jpg`


### Add avatar and intro text

Name your avatar image with the filename `avatar.jpg` and add it to your `static/images` folder, i.e. `static/images/avatar.jpg`. Or alternatively, you can change `avatar` in `config.toml` to its respective path and filename. Update `intro` to change the intro text. You can use markdown in `intro`.

```toml
[params.header]
  avatar = "images/avatar.jpg"
  intro = "This is **Visualize**, a responsive site template designed by [TEMPLATED](//templated.co)<br>and released for free under the Creative Commons License."
```


### Add gallery images

Data for all gallery images is stored in `data/gallery.toml`. Upload full and thumbnail size images to your `static` folder in any folder structure you wish. Use the following snippet below to add new images.

```toml
[[image]]
  full = "images/fulls/01.jpg"
  thumb = "images/thumbs/01.jpg"
  caption = "Lorem ipsum dolor sit amet 1"
```

Each image has a `caption` text. Update both `full` and `thumb` accordingly the image's respective file path.


### Additional settings

There are additional settings for the gallery lightbox functionality you can configure which are located in the [`static/assets/js/main.js`](//github.com/christianmendoza/hugo-visualize-theme/blob/master/static/assets/js/main.js) file.

```
$('.thumbnails').poptrox({
  onPopupClose: function() { $body.removeClass('is-covered'); },
  onPopupOpen: function() { $body.addClass('is-covered'); },
  baseZIndex: 10001,
  useBodyOverflow: false,
  usePopupEasyClose: true,
  overlayColor: '#000000',
  overlayOpacity: 0.75,
  popupLoaderText: '',
  fadeSpeed: 500,
  usePopupDefaultStyling: false,
  windowMargin: (skel.breakpoint('small').active ? 5 : 50)
});
```

The above are all default. Refer to the [jquery.poptrox documentation](//github.com/ajlkn/jquery.poptrox#config) for more configuration options. 


### Add social icon links

Add icons to your social media properties. Change `label`, `icon`, and `icon` accordingly. Follow the same snippet to add more icon links. Remove any of those you don't want.

```toml
[[params.social]]
  label = "Twitter"
  icon = "fa-twitter"
  url = "https://twitter.com"
```


### Add Google Analytics

Enable Google Analytics by adding your tracking id to `googleAnalytics`. Leave empty or remove if you don't want.

```toml
googleAnalytics = "UA-XXXXXXXX-1"
```


### Nearly finished

In order to see your site in action, run Hugo's built-in local server.

    $ hugo server

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/christianmendoza/hugo-visualize-theme/issues) to let me know. Or make directly a [pull request](//github.com/christianmendoza/hugo-visualize-theme/pulls).


## License

The original template is released under the [Creative Commons Attribution 3.0 License](//github.com/christianmendoza/hugo-visualize-theme/blob/master/LICENSE.md). Please keep the original attribution link when using for your own project. If you'd like to use the template without the attribution, you can check out the license option via the template [author's website](//templated.co/visualize).


## Annotations

- Original [Visualize](//templated.co/visualize) Template by [TEMPLATED](//templated.co)
- Demo Images by [Unsplash](//unsplash.com)

Also thanks to [Steve Francia](//github.com/spf13) for creating [Hugo](//gohugo.io) and the awesome community around the project.
