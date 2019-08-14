# Contents
Paper is based on the [Minima](https://github.com/jekyll/minima) theme (the standard Jekyll theme).
Please read the [Minima documentation](https://github.com/jekyll/minima/blob/master/README.md) for additional details.

### Layouts

Refers to files within the `_layouts` directory, that define the markup for your theme.

  - `default.html` &mdash; The base layout that lays the foundation for subsequent layouts. The derived layouts inject their contents into this file at the line that says `content` and are linked to this file via [FrontMatter](https://jekyllrb.com/docs/frontmatter/) declaration `layout: default`.
  - `default-wide.html` &mdash; A base layout that supports extra wide layouts.
  - `home.html` &mdash; The layout for your landing-page / home-page / index-page. [[More Info.](#home-layout)]
  - `doc.html` &mdash; The layout for your documentation pages.
  - `page.html` &mdash; The layout for your documents that contain FrontMatter, but are not posts.
  - `post.html` &mdash; The layout for your posts.

#### Home Layout

`home.html` provides a basic HTML layout for the site's landing-page / home-page / index-page. <br/>
Feel free to costumize it to your needs. Use that big brain of yours!

##### *Main Heading and Content-injection*

The *home* layout will inject all content from your `index.md` / `index.html` **before** the **`Posts`** heading. This will allow you to include non-posts related content to be published on the landing page under a dedicated heading. *We recommended that you title this section with a Heading2 (`##`)*.

Usually the `site.title` itself would suffice as the implicit 'main-title' for a landing-page. But, if your landing-page would like a heading to be explicitly displayed, then simply define a `title` variable in the document's front matter and it will be rendered with an `<h1>` tag.

##### *Post Listing*

It will be automatically included only when your site contains one or more valid posts or drafts (if the site is configured to `show_drafts`).

The title for this section is `Posts` by default and rendered with an `<h2>` tag. You can customize this heading by defining a `list_title` variable in the document's front matter.

### Includes

Refers to snippets of code within the `_includes` directory that can be inserted in multiple layouts (and another include-file as well) within the same theme-gem.

  - `head.html` &mdash; Code-block that defines the `<head></head>` in *default* layout.
  - `header.html` &mdash; Defines the site's main header section. By default, pages with a defined `title` attribute will have links displayed here.
  - `social.html` &mdash; Renders social-media icons based on the `minima:social_links` data in the config file.
  - `breadcrumbs.html` &mdash; Renders bredcrumbs based on the passed include variables **url** and **edit_url**.
  - `sidebar.html` &mdash; Renders a sidebar for navigating the docs.
  - `toc.html` &mdash; Renders a table of contents list.
