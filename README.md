# A website template for academics

This website was made from the template provided by [sbryngelson](https://github.com/sbryngelson).

## Fork and build

- Fork [the original repository](https://github.com/sbryngelson/sbryngelson.github.io) by clicking the `fork` button in the top-right corner of its Github page.
- Install [Jekyll](https://jekyllrb.com/docs/installation/) (version less than 4.0 required) on your local computer
- Run `$ bundle exec jekyll serve` in the repository root directory
- Your site is now hosted locally at `localhost:4000`, which you can access with your web browser.

Note:

- This webpage uses Jekyll plugins like Jekyll Scholar to automatically build your bibliography.
  If you are using GitHub pages, you will have to build the site with the `Rakefile` in the root directory of the source branch.
  You can do so by first modifying the file as appropriate and then, after pushing your changes, execute `rake publish`.

## Customization

- Modify `_config.yml` as appropriate
- Modify YAML database files, located in `_data/*.yml`, as appropriate
- Modify individual pages, located in `_pages/*.md`, as appropriate

### Navbar

The pages in the top navbar are in the `_config.yml` file.
The typical options are already included or commented on, though additional pages can be created and listed here.

### Creating or editing pages

All pages are located in the `_pages` directory.
Pages generally load information from YAML databases located as `_data/*.yml`.
Creating new pages can be done by using existing pages as a template.

#### Page header information

All pages require header information.
Example header data for the 'Talks' page is below.

```
---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /talks/
---
```

The `layout` variable corresponds to HTML layouts in the `_layouts` directory.
The difference between most layouts is subtle, and `gridlay` can generally be used.
The permalink must be unique for each page and correspond to the directory storing the page in the compiled HTML.
Refer to your pages in `_config.yml` via the `title` variable.

#### Markdown

All pages are written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) as `*.md`.
HTML commands and CSS styles can be directly used in a markdown files.

#### Publication page and database

The publications and talks are now listed via Jekyll Scholar.
The bibliography file `ref.bib` is located in the `assets/` directory.
Modify according to your needs.

## Hosting

Once your site has been modified to fit your needs, you should host it somewhere so others can access it.

### Github pages

A simple way to host your site for free is via [Github Pages](https://pages.github.com/).
This will provide you with a free domain name at your_github_username.github.io.
Instructions on how to do this are available on their page.
They generally involve creating a repository on your Github titled `your_github_username.github.io` and uploading your files there (everything except the `_site/` directory, which the GitHub Pages service will generate using its own version of Jekyll).
Then, GitHub will automatically rebuild your site every time you push a commit to the repository (no bundle/Jekyll commands required).

### Hosting elsewhere

If you already have a hosting service for a static HTML webpage, such as some universities provide, you can build your website locally using `bundle exec jekyll serve`.
Then, upload the resulting files to this server via SSH or FTP via the `_site/` directory.
Be sure that the `site.url` and `site.baseurl` are set appropriately in the `_config.yml` file.

## Acknowledgment

sbryngelson also credits the [Allen Lab](https://www.allanlab.org/) for creating a beautiful academic research group webpage.
Many parts of this site were adopted or copied from their laboratory webpage.

## License

MIT
