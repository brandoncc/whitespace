Whitespace
==========
Whitespace is a minimal and responsive theme for [Octopress](http://octopress.org). This theme lets your contents take the center stage of your blog.


Demos
-----


Default theme: [Themespace Preview](http://themespace.github.io/whitespace/)

Actual blogs: [Lucas Lew's blog](http://lucaslew.com), [Chymeric Tutorials](http://chymeric.eu), [Yous' Blog](http://yous.be/)

*If you are using whitespace and would like to showcase your website, we would be very happy to add you to the list! Just tell us your URL via the issue tracking system!*


Install
-------
    $ cd octopress
    $ git clone git://github.com/lucaslew/whitespace.git .themes/whitespace
    $ rake install['whitespace'] # for zsh, use: rake install\['whitespace'\] 
    $ rake generate


Update
------
    $ cd octopress/.themes/whitespace
    $ git pull
    $ rake install['whitespace']
    $ rake generate


Update and Keep Customizations
------------------------------
*For this to work, you have to track your website theme customizations on a remote (we call it ```mywebsiterepo```).*

    $ cd octopress/.themes/whitespace
    $ git pull
    $ rake install['whitespace']
    $ cd ../..
    $ git fetch --all
    $ git reset --hard mywebsiterepo/master
    $ rake generate


Comment System
--------------
We support the open-source [Juvia](https://github.com/phusion/juvia) comment system. To enable it, add the `juvia_site_key` and `juvia_host` parameters in `_config.yml`.


Navigation Bar
--------------
You can add several icons to the navigation bar. Just set the corresponding user IDs in `_config.yml`:

- `googleplus_user` with `googleplus_hidden: false` for Google+ profile.
- `pinboard_user` for Pinboard bookmarks.
- `delicious_user` for Delicious bookmarks.
- `github_user` with `github_show_profile_link: true` for GitHub profile.
- `bitbucket_user` for Bitbucket profile.


External URL
------------
You can also use our theme to set up a [Linklog](http://en.wikipedia.org/wiki/Linklog)! To publish a link post, just add the `external-url` variable to the YAML section (the header) of your post - and specify a valid URL.

    ---
    layout: post
    ...
    external-url: http://example.com/some/external/url
    ---

The title will be rendered with an arrow (&rarr;) character at the end; and the title link will point to the external url.

Google+ "authored by" link
------------------------
If the `googleplus_user` variable is set under `_config.yml`, by default, posts will contain a link with `rel="author"` pointing to the respective Google+ profile.

You can override the pofile for the authored by link for a specific post by adding `googleplus_user` for the post:  

    ---
    layout: post
    ...
    gooleplus_user: [put overriding profile id here]
    ---
	
You can also choose to ignore the link by assigning `ignore` to the `googleplus_user` post variable (in your post header). The "authored by" text will then be displayed without a link.

    ---
    layout: post
    ...
    gooleplus_user: ignore
    ---

License
-------
(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


