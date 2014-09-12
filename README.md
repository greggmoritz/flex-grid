
# CSS Flexbox Grid

A set of reusable CSS classes that can be used to easily construct interface layouts. This component is built on the [CSS3 Flexbox Layout module](http://www.w3.org/TR/css3-flexbox/). Benefits gained from this approach are (1) a simplified markup structure and (2) ability to leverage flexbox's alignment and distribution properties in a grid solution.

## Dependencies


* sass - http://sass-lang.com/install
* bourbon - http://bourbon.io/ (scroll to USAGE & INSTALLATION)

## Building

### CLI

Once installed, you can use the command line to compile Sass files to CSS.
See [Using Sass](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#using_sass) for compilation options. But to get started you can run the following command in you project's root directory:

	sass -fg --update [sass-src-directory]:[css-dest-dir] -t expanded


### Desktop Apps

There are a number of apps you can use to watch and compile your Sass (CoffeeScript, LESS, Stylus, etc.) files:

* [LiveReload](http://livereload.com/)
* [Hammer](http://hammerformac.com/)
* [Scout](http://mhs.github.io/scout-app/)
* ..and more

## Specs

This grid has the following properties:

1. Is fluid and will fill 100% of the available space
2. 12 columns (can be customized via Sass variable `$total-grid-columns`)
3. Gutters:
	* 20px between columns (can be customized via Sass variable `$grid-gutter-width`)
	* Columns have left/right padding equal to half the gutter width
	* Columns use border-box box model

## Usage

### Standard Grid

A grid is comprised of a grid container and grid columns. For example to make a grid with a 25% (3 of 12 cols) left column and 75% (9 of 12 cols) content area, use the following markup:

	<div class="grid">
		<div class="grid-col-3"></div>
		<div class="grid-col-9"></div>
	</div>

There is no need for row classes or markup. To achieve a grid with a "row" of 25%/75% and a 2nd "row" with 3 equal columns, you could write:

	<div class="grid">
		<div class="grid-col-3"></div>
		<div class="grid-col-9"></div>
		<!--
			No special markup is needed
			a new "row" will start when the sum of the columns exceeds 12 (`$total-grid-columns`)
		-->
		<div class="grid-col-4"></div>
		<div class="grid-col-4"></div>
		<div class="grid-col-4"></div>
	</div>


### Auto-fill Columns

### Offsetting Columns

### _n_-up Layouts

### Squashing Gutters

### Nesting

### Alignment

## Browser Support

* Chrome
* Firefox
* Safari
* IE 10/11
