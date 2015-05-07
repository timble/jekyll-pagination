![Jekyll Pagination](http://www.timble.net/images/blog/2015/jekyll-pagination.gif)

# Better pagination for Jekyll
A Jekyll `include` file of a Mobile-First pagination.

## Elements

![Pagination elements](http://www.timble.net/images/blog/2015/jekyll-pagination-elements.png)

Depending on screen size it shows:

1. Previous page link
2. First page
3. 'missing' pages indicator
4. x amount of pages before the current page
5. The current page
6. x amount of pages after the current page
7. 'missing' pages indicator
8. Last page
9. Next page link

## Installation

Install with bower: `bower install https://github.com/timble/jekyll-pagination.git`

## Options

The amount of pages shown can be set in your config.yml file using the `paginate_limit` setting. This setting shows this amount of pages PLUS the current page. So if you set it to `8` you will have 9 pages.

This setting is also used to calculate the amount of pages before and after the current page. When setting this to an uneven number it shows exactly this amount of pages. But when setting it to an even number it divides the number by 2 and places half before and half after the current page. The reason it works this way is to keep a balance in the pagination by showing as much pages left to it as it does right to it.

## SCSS variables

* All variables in the SCSS file are overwriteable.
* Only set `$pages-clearfix` to `false` if you're already using another `clearfix @mixin` in your prject which this file can access.
* All the styling variables are only applied when `$pages-cosmetics` is `true` (it's `true` by default)
* The breakpoint variables are to show or hide pages when the screen is smaller. Use with caution since more pages then wanted may get hidden.
