# Day 8 Notes - CSS Variables & Google Fonts

## CSS Variables (Custom Properties)

/*Define in :root (global scope)*/
:root {
    --primary-color: #8B0000;
    --accent-color: #D4AF37;
    --text-dark: #2c2c2c;
    --text-light: #6b6b6b;
    --bg-cream: #FFF8F0;
    --font-heading: 'Playfair Display', serif;
    --font-body: 'Lato', sans-serif;
    --spacing-sm: 10px;
    --spacing-md: 20px;
    --spacing-lg: 40px;
    --border-radius: 8px;
    --transition: all 0.3s ease;
}

/*Use them anywhere*/
.button {
    background-color: var(--primary-color);
    font-family: var(--font-heading);
    padding: var(--spacing-md);
    transition: var(--transition);
}

/* Benefits:

- Change entire theme by editing :root
- Consistent values everywhere
- Professional habit
*/

## Google Fonts in HTML
<!-- Add in <head> -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">

# Day 10 Notes - Multi-Page Sites

## File Path Examples
<!-- From root (index.html): -->
<a href="pages/menu.html">Menu</a>

<!-- From inside pages/ folder: -->
<a href="../index.html">Home</a>
<a href="about.html">About</a>  (same folder)

## Active Navigation State
Add class="active" to current page's nav link

## Shared Components Pattern
Copy navigation HTML to each page (for now)
Later we'll learn JavaScript to load it dynamically

## Menu Page Layout Plan
- Section 1: Hero banner (small)
- Section 2: Appetizers grid
- Section 3: Pasta & Main courses
- Section 4: Desserts
- Section 5: Drinks
Each section has title + menu items in grid

# Day 11 Notes - Pseudo-Elements

## ::before and ::after
These create fake elements inside other elements.
Used for decorative effects, icons, overlays.

h2::before {
    content: "";             /* REQUIRED (can be empty) */
    display: block;
    width: 40px;
    height: 3px;
    background-color: gold;
    margin-bottom: 10px;
}

/* Decorative quote marks */
blockquote::before {
    content: '"';
    font-size: 4rem;
    color: #ddd;
    line-height: 0;
}

## object-fit for images
img {
    width: 100%;
    height: 300px;
    object-fit: cover;    /* Fill without stretching */
    object-position: center top;  /* Where to focus */
}
