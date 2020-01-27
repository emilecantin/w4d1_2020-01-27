Intro to CSS
============

## Semantic HTML

Writing good CSS starts with writing good HTML.

Good HTML is Semantic; the markup actually has some meaning. Use `<aside>`, `<article>`, `<nav>` and `<footer>` instead of `<div>`.

Using these help screen readers and search engine bots understand your website better. This makes your website more accessible, and will rank you better on Google.

## Block-level vs inline elements

*Block Elements* grow to take the full width of their parent element, and each will display on a new line.

*Inline Elements* only take the width of their contents. As their name implies, they also display "in" a line.

You can place block or inline elements inside a block element, but you can only put inline elements in an inline elements.

## CSS Reset / Normalize

All browser ship with a default stylesheet that specifies the default look of the different HTML elements. However, there are some slight differences between them. A CSS Reset removes these differences.

## Anatomy of a CSS rule

A CSS rule is made of two things:
- A selector
- A list of properties

Example:
```css
nav#navbar.blue a {
  color: white;
}
```

See here for a full explanation: https://www.tutorialspoint.com/css/css_syntax.htm


## The box model and Box-Sizing

All elements in HTML are ultimately rectangles of different sizes. They all have a content area, surrounded by an empty space called *padding*, surrounded by a *border* of varying style, color and size, surrounded by more empty space called *margin*.

When you manually specify a width or height, it can have 2 different behaviours:
- If `box-sizing: content-box`, it sets the size of the content area (default)
- If `box-sizing: border-box`, it sets the size of the overall element, up to and including the margins.

## CSS Specificity & best practices

When styles conflicts, the more *specific* one wins. As a rule, IDs are the most specific, followed by classes, followed by element types.

The best practice is to write yous styles to be as specific as needed, but no more, because you might want to override it later. A good approach is to use a class or an id for particular part of your page, and then target its descendants using their element type. E.g `#navbar a` to target all the link in your navbar, `#navbar a.main` to target the "main" link in your navbar.

Use classes to make your styles reusable. E.g `.red`, to make somethingred, or `.featured` to make something stand out.

Also use classes to name your "components". E.g `.searchInput` for a search box or `.side-category` for a category grouping in your sidebar.

Use IDs to target unique parts of the webpage that you're absolutely, positively sure won't appear anywhere else on the page. E.g `#navbar` or `#login-form`. Even then, you can use classes instead without any ill effects.
