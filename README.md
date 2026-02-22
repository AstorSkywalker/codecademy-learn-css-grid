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

## Next Steps

Try experimenting with:
- `grid-template-rows` — explicitly define row heights
- `grid-gap` or `gap` — add spacing between grid items
- `grid-auto-flow` — change how items fill the grid (row vs. column)
- `grid-column` / `grid-row` — make items span multiple cells
