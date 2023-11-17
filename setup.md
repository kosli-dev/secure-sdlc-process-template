# Setting up the SDLC template for your process

This site is built with the [HUGO](https://gohugo.io/) static website framework, and is built on top of the [book theme](https://github.com/hotosm/hugo-book).

After forking the template, some steps need to be taken to make it your own.

## Updating config.toml

At the root of the directory is the config.toml file, which defines the Hugo sites settings.
The following settings may need to be updated:
- `baseURL`: the root url where this site will be published
- `title`: the title of the website, which will display in the header and various parts of the site
- `logo`, under `[param]`: the path to your logo (this file should be place in the static folder)

## Updating the content

All pages built are defined in the `content` folder. This directory and its subdirectories shape the left-hand navigation on the site itself.
Adding or removing a markdown file in these directories will add or remove the corresponding page of the site, and its entry in the navigation.
Some variables can be defined in the YAML front matter of each page, notably its `weight`, which defines its order in listings and in the navigation, and its `title`, which defines its name in the navigation.

In order to add a new section to the navigation, a new directory must be created in the relevant directory, and must contain a `_index.md` file, itself with the relevant YAML front matter.

## Running the site locally

To run the site locally, Hugo must be installed (see https://gohugo.io/installation/).
The following command builds the site and runs in on http://localhost:1313
```
hugo server --minify --theme hugo-book --cleanDestinationDir --gc
```

## Deploying the site

The website can be deployed to any platform that accepts Hugo builds, including popular platforms such as GitHub Pages, or Netlify. Some examples can be found in the [Hugo documentation](https://gohugo.io/categories/hosting-and-deployment/).

