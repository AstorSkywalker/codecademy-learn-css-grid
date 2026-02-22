# Codecademy CSS Grid

A learning project for understanding **CSS Grid**, a powerful layout tool for creating responsive two-dimensional grid layouts.

## Links

- **Repository:** https://github.com/AstorSkywalker/codecademy-learn-css-grid
- **Live Site:** https://astorskywalker.github.io/codecademy-learn-css-grid/

## What is CSS Grid?

CSS Grid is a layout system that allows you to define rows and columns, then position elements within that grid. Unlike Flexbox (which works in one dimension), CSS Grid handles both horizontal and vertical alignment, making it ideal for complex page layouts.

### Key Advantages
- **Two-dimensional layout control** — manage rows and columns simultaneously
- **Responsive design** — easily adjust grids for different screen sizes
- **Simplified complex layouts** — reduce the need for nested elements and float hacks
- **Precise positioning** — control exact placement of grid items

## CSS Grid Properties Used in This Project

### Container Properties (`.grid`)

| Property | Value | Purpose |
|----------|-------|---------|
| `display` | `grid` | Activates the CSS Grid layout mode |
| `grid-template-columns` | `100px 100px 100px` | Defines 3 equal columns of 100px each |
| `width` | `500px` | Sets the grid container width |
| `height` | `300px` | Sets the grid container height |
| `border` | `2px solid black` | Visual boundary around the grid |

### Item Properties (`.item1` - `.item5`)

- `background-color` — Visual styling with distinct colors for each item
- `border` — Visual separation with `2px dotted black` borders

## How the Grid Works

With `grid-template-columns: 100px 100px 100px`, the grid creates:
- **3 columns**, each 100px wide
- **Automatic rows** that adjust based on content
- **5 items** positioned left-to-right, wrapping as needed

### Example Layout
```
┌─────────┬─────────┬─────────┐
│ Item 1  │ Item 2  │ Item 3  │
├─────────┼─────────┼─────────┤
│ Item 4  │ Item 5  │         │
└─────────┴─────────┴─────────┘
```

## Files

- `index.html` — HTML structure with 5 grid items
- `style.css` — CSS Grid configuration and item styling
- `README.md` — This file

## Grid Row Properties

This project demonstrates row positioning using the following related properties:

- `grid-row-start`: the grid line where the item begins. Can be a number, a named line, or the keyword `span` (e.g. `grid-row-start: 2;` or `grid-row-start: span 2;`).
- `grid-row-end`: the grid line where the item ends. Typically used together with `grid-row-start` (e.g. `grid-row-end: 4;`).
- `grid-row`: shorthand for `grid-row-start / grid-row-end`. Examples:
	- `grid-row: 1 / 3;` — start at line 1, end at line 3 (spans two rows)
	- `grid-row: 2 / span 2;` — start at line 2 and span 2 rows

Project examples:

- `.item4` in `style.css` uses:
	- `grid-row-start: 1;`
	- `grid-row-end: 3;`
	This places the item starting on row line 1 and ending on row line 3, so it occupies both defined rows.

- In the blue example grid (`.grid10`), `.item20` demonstrates the shorthand:
	- `grid-row: 2 / 4;` — shorthand that places the item from row line 2 to row line 4 (spanning two row tracks).

When using these properties, keep in mind that grid line numbers start at 1 at the start edge of the grid and increase across rows; using `span` makes it easier to specify how many rows an item should cover without calculating the end line explicitly.

### Important note: grid lines vs rows

`grid-row-start` and `grid-row-end` refer to *grid lines* (the boundaries between rows), not the rows themselves. Grid lines are numbered from 1 at the start edge of the grid. For a grid with two row tracks, the top edge is line 1, the middle line between rows is line 2, and the bottom edge is line 3. So to place an item in the first row you would use `grid-row: 1 / 2` (start at line 1, end at line 2).

Using `span` is often more intuitive because it expresses how many row tracks an item should cover without calculating the ending line. Examples:

- `grid-row: 1 / span 2;` — start at line 1 and span two rows (equivalent to `1 / 3` when there are at least two rows)
- `grid-row-start: 2; grid-row-end: span 2;` — start on line 2 and cover the next two tracks

`span` is especially handy when items should grow or when you don't want to recalculate line numbers after changing the grid definition.

## Next Steps

Try experimenting with:
- `grid-template-rows` — explicitly define row heights
- `grid-gap` or `gap` — add spacing between grid items
- `grid-auto-flow` — change how items fill the grid (row vs. column)
- `grid-column` / `grid-row` — make items span multiple cells
