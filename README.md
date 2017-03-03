# About

This is a Jekyll site built to run as a Github pages Organization Pages site:

https://lookinglocal.github.io/

>Content from the master branch will be used to build and publish your GitHub Pages site.

This typically takes a few seconds after a commit is pushed.

Source: https://help.github.com/articles/user-organization-and-project-pages/

# Information for writers

Jekyll docs: https://jekyllrb.com/docs/posts/

FontAwesome cheat cheet: http://fontawesome.io/cheatsheet/

# Information for developers

This is forked from https://github.com/mmistakes/minimal-mistakes

# To run locally with Jekyll

Install dependencies using Bundler: `$ bundle install`

On Mac OS Sierra you may need to do something like this first:

`$ xcode-select --install`

`$ bundle config build.nokogiri --use-system-libraries --with-xml2-include=$(brew --prefix libxml2)/include/libxml2`

Start server: `$ bundle exec jekyll serve`

Or using overrides for local config `$ bundle exec jekyll serve -w --verbose -c _config.yml,_config.dev.yml --drafts`

Reference: https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/

## Keeping your local server up to date with the GitHub Pages gem

> Jekyll is an active open source project and is updated frequently. As the GitHub Pages server is updated, the software on your computer may become out of date, resulting in your site appearing different locally from how it looks when published on GitHub.
> 
> `$ bundle update github-pages` or simply 
> `$ bundle update` and all your gems will update to the latest versions.
> 
> If you don't have Bundler installed, run gem update github-pages

# GitHub Pages dependencies

If you want to find out versions of underlying components in GitHub Pages (e.g. Liquid templating engine), see:

https://pages.github.com/versions/

# Liquid templating engine

https://shopify.github.io/liquid/

Unfortunately the Liquid documentation isn't version-specific.
