# Example project integrating Assemble in an angular project

This project shows how to integrate the nice [Assemble](http://assemble.io/) project. The project is boostraped using the [Yeoman generator for Angular](https://github.com/yeoman/generator-angular) which follows a strict architecture. The only html page is the `index.thml` containing all the assets and scripts. Creating subsequent pages with Assemble brings a few challenge with:

- `usemin` and `useminPrepare` tasks: to keep the assets consistants accross the pages.
- `bower:install` and the `yo` scaffolders to keep them in the loop with new structure.

I opted for a general layout `layout.hbs` to act as the main point (much like `index.html` before) that each page will inherits assets and scripts. I removed the `htmlmin` task, because I hate it. (It never works really as expected) 

## Unsolved problems:

Static pages in a folder wouldn't refer correctly assets. See [this stackoverflow](http://stackoverflow.com/questions/18964875/how-should-i-configure-grunt-usemin-to-work-with-relative-path) and a possible workaround on [github](https://github.com/buddhike/grunt-usemin/commit/daefa9eb9ac498a17090008c48fb7392ab82d359#commitcomment-6062680)

## Future

I'll probably develop the concept to:

- compile certain angular views into static file (for older broswers that would not support angular features)
- Integrate Assemble's generated pages with angular's controller, e.g. creating a blog where a summary of the blog post is embed into angular, but the full post is a separate page.

Comments and advises are welcomed.
