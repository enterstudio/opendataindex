# Open Data Index

This is the code that powers the [Open Data Index](http://index.okfn.org/).


## Working with content

(WIP notes that will in turn be integrated with proper documentation)

### Collections

We use Jekyll's collections to implement our "custom" page types. 

We have the following collections:

* Pages (`/_pages`): (content editable) For generic pages such as about, methodology, etc. (We do pages in a collection rather than the standard 'pages' in Jekyll so that pages can be all nice and tidy in their own directory).
* Places (`/_places`): (will be generated from `_data`) Data discovery by place, and subsections thereof, such as place/dataset (e.g.: /australia; /australia/transport-timetables).
* Datasets (`/_datasets`): (will be generated from `_data`) Data discovery by dataset (e.g.: /transport-timetables).

In addition to Jekyll's builtins that we use:

* Posts (`_posts`): (content editable) For blog or news. etc. (could be removed, probably not required).

Note that everything under `_places` and `_datasets` will be autogenerated from `_data`, and should not be directly edited.

### Content includes

There are also pure content files under `_includes/content`. This will be used for various partial snippets throughout the site as the design progresses.

The naming of these files should give some indication as to their use in the site. 

### Info for adding content

#### Front matter

Jekyll uses YAML front matter to add content around the main content of a page.

There are a few metatags that ODI implements and uses, and content editors should be aware of them:

* key: a special identifier for a page, often used in CSS
* summary: often used as the meta description, which is displayed in search index results
* nav_show ('Pages' only): show or hide this page from the main site navigation
