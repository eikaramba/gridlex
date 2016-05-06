# Gridlex
## Just a Flexbox Grid System
v. 2.0.8

Based on the Flexbox grid from http://gridlex.devlint.fr/, i adapted it to be even more flexible. Now you can mix and switch sizes, position, offset and stretching declarations however you like, both for grid/column and each different responsive media query.

The concept is simple: you need to wrap your `.column` in a `.grid`.

### What can we expect?
- Basically each column is the same width as every other cell in the grid.
- But you can add sizing classes to individual columns.
- For responsive designs, you can add classes based on media-queries.
- Top, bottom, or middle. For the grid. And for the columns.
- Grids can be nested. Always. Directly in a column.

### Less, Sass, CSS?

**I just wanna use it in my page!**

To use Gridlex out of the box, call the gridlex.min.css file in your project :

Via cdnjs:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/gridlex/2.0.8/gridlex.min.css">
```

Via jsdelivr:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gridlex/2.0.8/gridlex.min.css">
```
**I want to include it in my source files!**

Because I'm working with Less, Gridlex comes first in Less (with less-compilation Grunt task).

But there is the same version in Sass in the `src` folder.

Include gridlex/src/gridlex.less or gridlex/src/gridlex.scss

### 3 ways to use Gridlex
**1- The basic. Just add a class `.grid-*` (from -1 to -12)**
```html
<div class="grid-1">
	<div class="column">...</div>
</div>
```

**2- The precise. Compose cell by cell (with class like `.column-*`)**
```html
<div class="grid">
	<div class="column-12">...</div>
</div>
```

**3- The automatic. Just add number of cells you want in the grid (`.grid > .column`)**
```html
<div class="grid">
		<div class="column">...</div>
		<div class="column">...</div>
</div>
```

### Gridlex and media-queries
Because of responsive, you sometimes need to change the size of columns: with this html markup you can change that:
<table>
<thead>
	<tr>
		<th>CSS Media Query</th>
		<th>Applies</th>
		<th>Usage/Tag</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td><code>@media screen and (max-width: 35.5em)</code></td>
		<td>Max 568px</td>
		<td><code><b>small</b>="*"</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (max-width: 48em)</code></td>
		<td>Max 768px</td>
		<td><code><b>medium</b>="*"</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (max-width: 64em)</code></td>
		<td>Max 1024px</td>
		<td><code><b>large</b>="*"</code></td>
	</tr>
	<tr>
		<td><code>@media screen and (max-width: 80em)</code></td>
		<td>Max 1280px</td>
		<td><code><b>huge</b>="*"</code></td>
	</tr>
</tbody>
</table>

## Install
### npm
npm install gridlex --save

### bower
bower install gridlex --save


See more : http://gridlex.devlint.fr
