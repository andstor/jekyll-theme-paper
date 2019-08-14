# Setup project docs

#### Add project

To add project documentation, one must do the following
Create a `docs` folder if it doesn't already exists.
Inside it, create a new folder to hold the actual documentation files (mainly Markdown files). Name the folder the same as the project name. 

The docs folder structure should look this:

```
/docs/
├── project-1
├── project-2
└── ...
```
#### Documentation landing page

Every project needs an index.html file.
This serves as a landing page for the documentation of the specific project.

Set the file front matter `layout` to `doc`, and `repo` to the name the project name.

Define the variable `start_page` to use an existing documentation page as the initial page. For example `home.md`. 

One may choose to create a costom landing page.
Just don't include the `start_page` front matter variable, and any contents to this page will be displayed on the page.

#### Project data

Create a `_data` folder if it doesn't already exists.


##### Types

Inside the `_data` folder, create a types.yml file.
Here you define the project types you want to define. 
```
type:
  name: type_name
  description: Some descriptive text.
```

##### Projects

Inside the `_data` folder, create a projects.yml file.
Here you add info about the project(s) you want to add documentaion for. 

Each project should have the following structure:
```
project_name:
  name: display_name
  repo_name: repository_name
  type: 
    - type1
    - type2
  owner: owner_name
  url: repository_url
  wiki_url: repository_wiki_url
  icon: icon_picture_location
```

Note that a project may have several types.

###### Wiki

If you define a wiki [type](#types), this will show up on the  home page and will be excluded from the documentation page.
You may add a link in the navigation header by linking to the index.html file for the wiki type project. See [Customize navigation links](#customize-navigation-links)
```
wiki:
  name: wiki_name
  description: Wiki description
```

#### Default front matter
 
 Some front matter variables are required for all the documentation files.
 These are configured in the `_config.yml` file, with one entry per project.
 
 ```
 -
  #   scope:
  #     path: "docs/capquiz"
  #   values:
  #     layout: "doc"
  #     repo: "capquiz"
```
