# Why Ghost

Been using wordpress for a year or two. Good part about wordpress is plethora of hosting service and the plugin & theming ecosystem. Being slow was not a big deal, customization was. I am sure wordpress is customizable, just that I am not familiar with php and architecture.  

Couple of days back I have started migrating techincal and setup related docs(which I had added as a blog in wordpress) to this repo and maintain them as markdown files, things became much more easier to build and maintain. Markdowns are better with code snippets and link to a [praticular section of the file](https://github.com/aptro/stack/blob/master/development/rails/setup_pagination_kaminari.md#2-configure-kaminari-as-an-initializer) for sharing.

What is left is to figureout a platform to communicate ideas in longform. Ghost caught my eye to pick as a potential replacement for wordpress. It has a beautiful and clean publisher platform. Bonus point, written in Nodejs and my familiarity with nodejs. It opened the option to tinker around the platform.

Ghost has a cli which is like a toolkit for setup, maintance and upgrades. It has a way to setup a local instance where you can play around with the publisher platform, themes, look and feel of the blog. The local setup helped eliminate queries around tooling, production setup, customization.

After playing around with their local setup, figured out that the defaults with Casper theme was good enough for me without any customization. Ghost a wordpress plugin to migrate data and then import into local ghost setup. After play around for a while convinced that ghost is the right choice!

As of now [aptro.me](https://aptro.me) running on ghost. Here the [production setup](aptro_me_setup.md).

## Reference

1. [Feature to feature comparision between wordpress](https://ghost.org/vs/wordpress/)