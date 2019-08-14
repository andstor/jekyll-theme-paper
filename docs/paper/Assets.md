# Assets

Refers to various asset files within the `assets` directory.
Contains the `css/style.scss` that imports sass files from within the `_sass` directory. This `css/style.scss` is what gets processed into the theme's main stylesheet `main.css` called by `_layouts/default.html` via `_includes/head.html`.

This directory can include sub-directories to manage assets of similar type (`img`, `fonts`, `svg`), and will be copied over as is, to the final transformed site directory.
