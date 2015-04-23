# jekyll-pagination
A Jekyll `include` file to have advanced pagination.

Depending on screen size it shows:
* Previous page link
* First page
* 'missing' pages indicator
* x amount of pages before the current page
* The current page
* x amount of pages after the current page
* 'missing' pages indicator
* Last page
* Next page link

## Example

[previous] [1] ... [4] [5] [6] -7- [8] [9] [10] ... [20] [next]

## Options
The amount of pages shown can be set in your config.yml file using the `paginator-limit` setting. This setting shows this amount of pages PLUS current page. So if you set it to `8` you will have 9 pages.

## SCSS variables
* All variables in the SCSS file are overwriteable.
* Only set `$pages-clearfix` to `false` if you're already using another `clearfix @mixin` in your prject which this file can access.
* All the styling variables are only applied when `$pages-cosmetics` is `true` (it's `true` by default)
* The breakpoint variables are to show or hide pages when the screen is smaller.