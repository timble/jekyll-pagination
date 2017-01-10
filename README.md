![Jekyll Pagination](http://www.timble.net/images/blog/2015/jekyll-pagination.gif)

# Better pagination for Jekyll
A Jekyll `include` file of a Mobile-First pagination, configurable with page front-matter.

## Elements

![Pagination elements](http://www.timble.net/images/blog/2015/jekyll-pagination-elements.png)

Depending on screen size it shows:

1. Previous page link
2. First page
3. 'inivisible' pages indicator
4. x amount of pages before the current page
5. The current page
6. x amount of pages after the current page
7. 'invisible' pages indicator
8. Last page
9. Next page link

## Installation

Install with bower: `bower install https://github.com/timble/jekyll-pagination.git`

## Options

You can configure the output using front-matter on blog index page (for example `/blog/index.html`). The following options are available:

```html

---
paginate:
    root: /blog/
    limit: false
    page_amount: 7
    title_label: Pagination
---

```

- **root:** The root of your blog.
- **limit:** Limit of pagination pages, set to false if you want to use the page_amount setting.
- **page_amount:** The amount of pages visible in the pagination. Set to an uneven number for best result.
- **title_label:** The title above pagination (only visible for screen readers)

Because the front-matter is applied to the blog index page rather than the `_config.yml` it is possible to have multiple blogs on your site. You might need an additonal category aware pager plugin to accomplish this. 

## SCSS variables

* All variables in the SCSS file are overwriteable.
* Only set `$pages-clearfix` to `false` if you're already using another `clearfix @mixin` in your prject which this file can access.
* All the styling variables are only applied when `$pages-cosmetics` is `true` (it's `true` by default)
* The breakpoint variables are to show or hide pages when the screen is smaller. Use with caution since more pages than wanted may get hidden.

## In action

* [www.timble.net/blog/](http://www.timble.net/blog/)
* [www.joomlatools.com/blog/](https://www.joomlatools.com/blog/)
* [www.joomlatools.com/developer/blog/](https://www.joomlatools.com/developer/blog/)
