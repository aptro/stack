# Why Ghost

Have been using wordpress for a year or two. Good part about wordpress is the plugin & theming ecosystem. Being slow was not a big deal for me, customization was. I am sure wordpress is customizable, just that I am not familiar with php and the architecture.  

Couple of days back I have started migrating techincal and setup related docs(which I had added as a blog in wordpress) as markdown pages to this repo, things became much more easier to write and maintain. 
Markdown is better with code snippets and link to a [praticular section of the file](https://github.com/aptro/stack/blob/master/development/rails/setup_pagination_kaminari.md#2-configure-kaminari-as-an-initializer) for sharing.

What is left is to figureout a platform to communicate ideas in longform. Ghost caught my eye as a potential replacement for wordpress. It has a beautiful and clean publishing platform. Bonus point, Ghost is written in Nodejs and my familiarity with Nodejs. It opened the option to tinker around the platform, theming and stuff.

Ghost ships a cli toolkit for local setup and production setup, maintance and upgrades. The local setup helped me eliminate queries around tooling, production look and feel, customization. Also ported few of the blogs from wordpress to my local instance before migrating to production.

Ghost has a wordpress plugin to migrate data from wordpress. And allows you to upload the data to your ghost instance.

As of now [aptro.me](https://aptro.me) running on Ghost. Here the [production setup](aptro_me_setup.md).

## Reference

1. [Feature to feature comparision between wordpress](https://ghost.org/vs/wordpress/)
