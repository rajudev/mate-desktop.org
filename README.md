# mate-desktop.org

This repository contains the [Nikola](http://getnikola.com) configuration and
content for <http://mate-desktop.org>.

# Contributing content

If you want to add or edit content on <http://mate-desktop.org>, please submit
a [pull request](https://help.github.com/articles/using-pull-requests).

## Contributing a new post

Contributing a new blog post to the mate-desktop.org website is simple.

  * [Fork](https://help.github.com/articles/fork-a-repo) this repository.
  
  * Copy `blog/20991231markdown-template.md` to a new file. For example:

    cp blog/20991231template-markdown.md blog/20131107my-cool-blog-post.md

  * Edit your new file, making sure to change the metadata in the file header. The following are valid metadata fields and what they're for. 
    * `link` is optional, but should include the URL to the original article if there is one.
    * `description` is optional, and should briefly describe the post.
    * `tags` are any tags that are relevant. **You must include the `draft` tag.**
    * `date` is the intended publication date of the post in the format YYYY/MM/DD HH:MML:SS
    * `title` is the post title
    * `slug` is how the post name will be represented in the URL. **Make sure you modify the ``date`` prefix**.
    * `author` is your full name.

  * Commit your changes, [submit a pull request](https://help.github.com/articles/creating-a-pull-request) and one of the website maintainers will review your submission and publish it if it is suitable.

If you prefer ReStructuredText to Markdown, then follow the same process as
above, but use `blog/20991231rest-template.rst` as the template file.

### Embedding images

Markdown and reStructured Test both have markup for embedding images. To embed
an image, just drop your correctly sized image into the
`files/assets/img/blog/` directory and then link to it. When linking to an
image assets you drop the `'files` prefix from the Markdown and reStructured
Text markup.

#### Markdown image example

    ![MATE](/assets/mate-128.png)

#### reStructured Text image example

    .. image:: /assets/mate-128.png
        :align: center

### Submitting posts for future publication

The `date` field in the metadata also controls when a post will be published.
If you have created a post that should be published at a specific date or time,
set the date/time accordingly and that post will not be published until that
time.

The mate-desktop.org website is redeployed every 10 minutes, so the actual
publication time will be accurate to the nearest 10 minutes.

### Preventing a post from being published

If you have a post you are working on but do not wish to publish, just add
**draft** to the list of `tags` in the metadata. Posts tagged as *draft* will
not be published.

## Contributing a translation

To contribute a translated page or blog post to the mate-desktop.org website do
the following:

  * [Fork](https://help.github.com/articles/fork-a-repo) this repository.

  * Copy the blog post or page you wish to translate to a new file with the same
  filename but ending with the short country code (see below). For example, if
  you want to translate the home page to German you would do the following:

    cp pages/index.md pages/index.de.md

  * Translate the metadata as well as the content. However, **do not change the date format**.

  * Commit your changes, [submit a pull request](https://help.github.com/articles/creating-a-pull-request)
  and one of the website maintainers will review your submission.

Nikola supported languages are, the one in bold are already in the site navigation::

  * `bg`     Bulgarian
  * `ca`     Catalan
  * `de`     **German**
  * `el`     Greek
  * `en`     **English**
  * `eo`     Esperanto
  * `es`     **Spanish**
  * `fa`     Persian
  * `fr`     **French**
  * `hr`     Croatian
  * `it`     **Italian**
  * `jp`     Japanese
  * `nl`     **Dutch**
  * `pt_br`  Portuguese (Brasil)
  * `pl`     Polish
  * `ru`     Russian
  * `tr_tr`  **Turkish** (Turkey)
  * `zh_cn`  Chinese (Simplified)

## Markdown vs. ReStructured Text

mate-desktop.org converts Markdown or reStructured Text into HTML. In general
we recommend Markdown, but some of the Nikola advanced features are only
exposed via reStructured Text extension.

### Markdown

Nikola follows the [syntax
rules](http://daringfireball.net/projects/markdown/syntax) of the original
`markdown.pl` with the following
[extensions](http://pythonhosted.org/Markdown/extensions/index.html) enabled:

  * `extra`
  * `codehilite`
  * `toc`

### reStructured Text

See the Nikola [reStructuredText Primer](http://getnikola.com/quickstart.html) and
the [reStructured Text extensions](http://getnikola.com/handbook.html#restructuredtext-extensions).

# Creating a Nikola stack

For the MATE Desktop core team, if you need to create a Nikola stack
for testing/deployment the installation process is documentation
for Ubuntu (also works in Debian Jessie) here:

  * https://flexion.org/posts/2015-11-installing-nikola-on-ubuntu/

# TODO

  * Add more text to the homepage.
    * Floating MATE logo
    * All the applications, with improved layout.
  * Integrate SocialSharePrivacy
    * https://github.com/panzi/SocialSharePrivacy
