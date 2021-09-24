### html5up-dopetrope

[Pelican](https://github.com/getpelican/pelican/) theme based on [html5up dopetrope](https://html5up.net/dopetrope) design.

## Preview
![](https://raw.github.com/PierrePaul/html5-dopetrope/master/screenshot.png)

Demo: <http://hopitaux-a-defendre.github.io/ghm-grenoble/>

## Features

* Responsive design, with a collapsible lateral navigation menu on mobile
* Pins on the homepage board can be either internal articles or simple external links
* Metadata to display "social share vignettes" of the website: support for [Open Graph](http://ogp.me) & [Twitter Summary Card](https://dev.twitter.com/cards/types/summary)
* i18n, with embeded localization in French
* Optional Google Analytics
* W3C-Validated HTML
* Optional "robots-noindex"
* Small:
```
$ du -ch static/{css,js}/ templates/
32K     templates/
153K    static/css/
196K    static/js/
381K    total
```

## Custom configuration variables

Optional variables are available for this theme :

*  `ADDRESS` : Your postal address. Accepts HTML.
*  `MAIL` : Your email address.
*  `PHONE` : Your phone number.
*  `TWITTER_USER` : 'Pierre_Paul', should be the url following http://twitter.com/
*  `GOOGLEPLUS_USER` : '110831175850960549188', should be the url following http://plus.google.com/ when viewing your profile.
*  `LINKEDIN_USER` : 'pierre-paul-lefebvre/2/9b7/aa' #Again, should be the URL following http://linkedin.com/ when viewing your profile.
*  `FACEBOOK_USER` : 'pierrepaul.lefebvre', if set in your profile, your profile can be accessed with a simple url like : https://facebook.com/pierrepaul.lefebvre
*  `ABOUT_TEXT` : Any text set here will show up on the bottom right of the page.
*  `ABOUT_IMAGE` : Image to show at the bottom right of the page.
*  `ABOUT_LINK` : Will add a link under the `ABOUT_TEXT` page 
*  `COPYRIGHT` : optional copyright notice that will appear in the footer
*  `DISPLAY_HOMEPAGE_ON_MENU` : you can set it to `True` to include a "HomePage" link in the navigation menu
*  `DISABLE_LATEST_ARTICLES` : you can set it to `True` to hide the "latest articles" section.
*  `FAVICON` : optional relative path to an image
* `META_IMAGE`: optional absolute URL of a custom image for the `og:image` meta property,
Twitter summary card, and `image` meta property of Schema.org.
This image is used in every page of the blog. Articles and pages can override the default
`META_IMAGE` by setting the `Image` metadata in the relative file.
* `META_IMAGE_TYPE`: the MIME type for `META_IMAGE`, this is needed for `og:image:type`.
* `NOINDEX`: can optionally be set to `True` to insert a `<meta name="robots" content="noindex">` meta tag

Articles can optionally define a `Link` metadata entry, instead of having content:
in this case, the corresponding article "box" on the homepage will point to that URL,
not to the internal article page.

## Developping the theme

It currently uses [SkelJS v0.3.3](https://github.com/ajlkn/skel),
a lightweight framework for building responsive sites.

### Updating translations

Summarizing [i18n_subsites plugin documentation](https://github.com/getpelican/pelican-plugins/blob/master/i18n_subsites/localizing_using_jinja2.rst#3-extract-translatable-strings-and-translate-them):

1. **Install Babel**:

    pip install Babel

2. **Extract translatable strings from `templates/*.html` into `messages.pot`**:

    pybabel extract --mapping babel.cfg --output messages.pot .

3. **Update the `.po` files based on `messages.pot`**:

    pybabel update --input-file messages.pot --output-dir translations/ --domain messages

Translation strings can now be manually edited in the `.po` files.

4. **Compile the `.po` files into `.mo` binaries**:

    pybabel compile --directory translations/ --domain messages

## License

[Creative Commons Attribution 3.0 Unported](https://raw.github.com/PierrePaul/html5-dopetrope/master/LICENSE.txt)
