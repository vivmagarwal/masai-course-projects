# Best Practices for Converting Figma Designs to HTML/CSS

When converting Figma designs to HTML/CSS, it's crucial to follow best practices to ensure a responsive and stable layout. Here's a guide with common pitfalls (bad examples) and how to correct them (good examples), perfect for beginners.

**Avoid Absolute Positioning**

If possible don’t use position absolute at all. Try to search for an alternative. Absolute positioning removes elements from the normal document flow, causing them to overlap or become misaligned at different screen sizes. Instead, use relative positioning, which positions an element relative to its normal position, or static positioning, the default for most elements.

- *Bad*: Positioning a button with `position: absolute; top: 10px; left: 200px;`. This might look fine on one screen size but can lead to overlapping or misaligned elements on others.
- *Good*: Use `position: relative;` for parent elements and `position: absolute;` for child elements when necessary, ensuring they move together.

**Avoid Hardcoding Height and Width**

Hardcoding dimensions in pixels can cause elements to lose their responsiveness. Hardcoding dimension makes layout very fragile.

- *Bad*: Setting an image with `width: 500px; height: 300px;`. This makes the image non-responsive, leading to layout issues on different screen sizes.
- *Good*: Use `width: 100%; height: auto;` for images, allowing them to resize proportionally within their container.

**Ensure Layout Doesn't Break on Zoom**

Users may zoom in for better readability, and the layout should remain intact. Regularly test your website at different zoom levels to ensure compatibility.

- *Bad*: Text overflowing its container when zooming in, indicating fixed pixel sizes are used.
- *Good*: Use relative units like `em` or `%` for font sizes and container widths to ensure scalability.

**Use Standard Containers**

- *Bad*: Using different width settings for each section, creating inconsistency across the website.
- *Good*: Use a consistent class-based container like `.content-container` across sections to maintain uniform width and margins.

**Use CSS Grid or Flexbox for Complex Layouts**

CSS Grid is ideal for two-dimensional layouts (rows and columns), while Flexbox is great for one-dimensional layouts (either a row or a column).

- *Bad*: Using complex float-based layouts, which are hard to maintain and less responsive.
- *Good*: Use Flexbox for linear layouts (like menus) and CSS Grid for two-dimensional layouts (like photo galleries).

**Make Use of CSS Variables**

CSS variables (custom properties) are useful for storing values you want to reuse throughout your document.

- *Bad*: Repeatedly using the same color code, like `#ff4500`, in multiple CSS rules.
- *Good*: Define a CSS variable `-main-color: #ff4500;` and use `var(--main-color)` throughout your CSS for easier maintenance.

**Use Semantic HTML**

Semantic HTML elements like **`<article>`**, **`<aside>`**, **`<details>`**, **`<figcaption>`**, **`<figure>`**, **`<footer>`**, **`<header>`**, **`<main>`**, **`<mark>`**, **`<nav>`**, **`<section>`**, **`<summary>`**, and **`<time>`** describe their meaning to both the browser and the developer, aiding in accessibility and SEO.

- *Bad*: Using `<div>` for every element, which provides no context about its content.
- *Good*: Use semantic elements like `<header>`, `<nav>`, `<footer>`, `<article>`, and `<section>` for better structure and accessibility.

**Follow the Mobile-First Approach**

Start with a design that fits mobile screens and then gradually enhance it for larger screens using media queries. This approach is more effective (in my humble opinion) in the current mobile-dominated internet usage.

- *Bad*: Designing for desktop first, leading to a cramped and inefficient mobile layout.
- *Good*: Start with mobile layout design and then use media queries to progressively enhance the design for larger screens.

**Incorporate Accessibility from the Start**

Ensure that your website is usable by everyone, including people with disabilities. This includes proper color contrasts for visibility, keyboard navigation, screen reader compatibility, and meaningful alt texts for images.

- *Bad*: Using color combinations with low contrast and not providing alt text for images.
- *Good*: Ensure sufficient color contrast and include descriptive alt text for images, like `alt="Logo of XYZ Company"`.

By avoiding these common pitfalls and following the good examples, you’ll create web pages that are not only visually appealing but also functionally robust and accessible. Remember, good web design is about more than just looks; it’s about creating an intuitive and seamless user experience across all devices.

## Resources

Github: https://github.com/vivmagarwal/masai-course-projects [source code]

Live Demo: [https://tiny-plum-crow-cuff.cyclic.app/](https://tiny-plum-crow-cuff.cyclic.app/) 

Figma 1: https://www.figma.com/file/P728ZEPqIwLTH6OTsqcJcD/Responsive_Template?type=design&node-id=0-1&mode=design&t=cGEUEnsvmqrx8riq-0 

Figma 2: [https://www.figma.com/community/file/1326961223815845862](https://www.figma.com/community/file/1326961223815845862) 

Responsive layout: [https://codepen.io/drupalastic/pen/dyJgBVK?editors=1100](https://codepen.io/drupalastic/pen/dyJgBVK?editors=1100)