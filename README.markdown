# ArcticConnect Platform Documentation

This repository contains the documentation for the ArcticConnect platform.

## Project Information

ArcticConnect is a network-enabled platform for realizing geospatial referencing of information about the arctic system derived from research, education, and private sector activities in the arctic and subarctic.

The ArcticConnect project is a collaboration between the Arctic institute of North America, CANARIE, Cybera, the GeoSensorWeb Lab, and the University of Calgary.

## Editing the Site

The source of all the pages and posts on the [site](http://geosensorweblab.github.io/ArcticConnect/) are in this repository. When the pages and posts are updated and pushed to GitHub then GitHub Pages will automatically update the site with the new information. This does not require any special software on your machine aside from a Git client. You can even do the editing through the GitHub interface, although I would not recommend this as there is no way to preview changes to make sure they display correctly.

To preview your changes before pushing to GitHub you will need to install Ruby and Jekyll on your machine. Check out the [Ruby install instructions](https://www.ruby-lang.org/en/documentation/installation/) for your platform, and try to install 2.0 or newer.

With Ruby installed you can clone the site repository to your machine using Git. Open a terminal or Git Bash shell and clone the repo.

    $ git clone git@github.com:GeoSensorWebLab/ArcticConnect.git

This will create a directory named ArcticConnect with all the site assets and Git history/settings. Next enter the directory and check for Ruby.

    $ cd ArcticConnect
    $ ruby -v
    ruby 2.2.1p85 (2015-02-26 revision 49769) [x86_64-darwin14]

The output will vary depending on your machine. The version of Ruby is not too important, as long as it is 2.0 or newer. If you get a message about `ruby` not being found or an unknown command, then your shell is not able to find the Ruby executable.

Next we [install Jekyll](http://jekyllrb.com/docs/installation/). Follow their instructions and make sure the `jekyll` command works.

```
    $ jekyll
    A subcommand is required.
    jekyll 3.0.0 -- Jekyll is a blog-aware, static site generator in Ruby

    Usage:

      jekyll <subcommand> [options]

    Options:
            -s, --source [DIR]  Source directory (defaults to ./)
            -d, --destination [DIR]  Destination directory (defaults to ./_site)
                --safe         Safe mode (defaults to false)
            -p, --plugins PLUGINS_DIR1[,PLUGINS_DIR2[,...]]  Plugins directory (defaults to ./_plugins)
                --layouts DIR  Layouts directory (defaults to ./_layouts)
                --profile      Generate a Liquid rendering profile
            -h, --help         Show this message
            -v, --version      Print the name and version
            -t, --trace        Show the full backtrace when an error occurs

    Subcommands:
      build, b              Build your site
      clean                 Clean the site (removes site output and metadata file) without building.
      doctor, hyde          Search site and print specific deprecation warnings
      help                  Show the help message, optionally for a given subcommand.
      new                   Creates a new Jekyll site scaffold in PATH
      serve, server, s      Serve your site locally
```

This is the correct output. Now you can run the local server to preview your changes.

    $ jekyll server

And open [http://localhost:4000/ArcticConnect/](http://localhost:4000/ArcticConnect/) to preview the site changes. Once your changes look good, use Git to commit them to your local repository and then push those changes to GitHub on the `gh-pages` branch.

## Writing Posts

Posts can be written with a mixture of Markdown and HTML. They are kept in the `_posts` directory and the name of the file is the slug in the URL with the date included. Dates are in ISO8601 order. Be sure to include the following stanza at the top of the post to customize the date and page title:

    ---
    layout: post
    title: "Technical Blog Started"
    date: 2015-10-29
    categories:
    ---

Changing the layout could be used to have a special layout for certain posts.

## Acknowledgements

This site is based on the ["Polar Bear" theme](https://github.com/diezcami/polar-bear-theme) by Camille Diez ([@diezcami](https://github.com/diezcami)).
