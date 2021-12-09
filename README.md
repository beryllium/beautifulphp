Beautiful PHP
=============

Everyone loves to bash PHP. Like any workhorse, it gets little praise when it works properly, and all the blame when something goes wrong.

Also, most people who bash it seem to believe the language hasn't changed in ten years.

It's time to end the misconception, and you can help!

If you've seen beautiful PHP code in the wild, consider submitting an example. Alternatively, you could contribute a clean and concise demonstration of programming concepts through the lens of PHP.

If you find you're always getting into arguments about one methodology over another (such as the ever-popular "That's Not MVC" or "You're doing OOP wrong"), maybe you could contribute a reference sample that everyone could learn from.

---

## Running the site locally

This site is powered by [Sculpin](https://sculpin.io/), a PHP static site generator.

After forking & cloning the repository, use [Composer](https://getcomposer.org/) (PHP's dependency manager) to install dependencies by running `composer install`.

To build the static site and serve it locally, watching for changes, run:

```
vendor/bin/sculpin generate --watch --server
```

Then, you can modify `source/index.html` or other files as necessary to make the changes you'd like to make.

## The way it's tied together

The site exists currently as one big [RevealJS](https://revealjs.com/) presentation. A whole bunch of sections come together to make it work as a slideshow. Navigation is usually right arrow for next slide, but some slides have extra detail that can be accessed by using the down arrow. Those ones show up in the HTML as nested sections.

New full pages can be added, but it would require creating a new file in the `source/_views` directory to adjust the styling. If you do want to add pages, you could use Markdown files with YAML front matter to customize them.

For example, after creating something like `source/_views/page.html`, you could add a new page by creating the file `source/demo.md`:

```
---
layout: page
title: My Demo Page
---
## My Demo Page

This is my demo page.
```

This page would then live at www.beautifulphp.com/demo/