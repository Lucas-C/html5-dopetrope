### html5up-dopetrope

[Pelican](https://github.com/getpelican/pelican/) theme based on html5up-dopetrope design.

## Preview
![](https://raw.github.com/PierrePaul/html5-dopetrope/master/screenshot.png)

Demo: <http://hopitaux-a-defendre.github.io/ghm-grenoble/>

## Variables

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
*  `COPYRIGHT` : If `SHOW_COPYRIGHT` is not set to `False`, it will show the copyright for html5up, credits for the images and the name set in this variable. You may want to set this variable to your name.
*  `SHOW_COPYRIGHT` : `True` by default, you can set it to `False` to hide the copyrights.
*  `DISABLE_LATEST_ARTICLES` : you can set it to `True` to hide the "latest articles" section.
*  `FAVICON` : optional relative path to an image
* `META_IMAGE`: optional absolute URL of a custom image for the `og:image` meta property,
Twitter summary card, and `image` meta property of Schema.org.
This image is used in every page of the blog. Articles and pages can override the default
`META_IMAGE` by setting the `Image` metadata in the relative file.
* `META_IMAGE_TYPE`: the MIME type for `META_IMAGE`, this is needed for `og:image:type`.
* `DESCRIPTION`: optional header text describing the website
* `NOINDEX`: can optionally be set to `True` to insert a `<meta name="robots" content="noindex">` meta tag

Articles can optionally define a `Link` metadata entry, instead of having content:
in this case, the corresponding article "box" on the homepage will point to that URL,
not to the internal article page.

## Updating translations
_cf._ https://github.com/getpelican/pelican-plugins/blob/master/i18n_subsites/localizing_using_jinja2.rst#3-extract-translatable-strings-and-translate-them

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

  [1]: https://github.com/getpelican/pelican/ "Pelican"
  [2]: https://raw.github.com/PierrePaul/html5-dopetrope/master/screenshot.png
  [3]: https://raw.github.com/PierrePaul/html5-dopetrope/master/LICENSE.txt
