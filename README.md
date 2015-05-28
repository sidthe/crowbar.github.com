# Crowbar

This is the repository for generating and managing the landing page of the
Crowbar project, you can reach it at http://crowbar.github.io.


## Build

In order to update the content of this website you need locally a working Ruby
environment. The dependencies are managed through Bundler, the content gets
generated with some simple Rake commands.

You need to install the dependencies only initially with ```bundle install```,
afterwards whenever you want to publish new content you just have to execute
```bundle exec rake publish```. To be able to publish new content you need
write access to this repository of course.

For local development and testing you can run ```bundle exec jekyll serve``` to
access a local running dynamic instance of Jekyll.
