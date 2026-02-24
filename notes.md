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

/*Use in CSS*/
font-family: 'Playfair Display', serif;
font-family: 'Lato', sans-serif;
