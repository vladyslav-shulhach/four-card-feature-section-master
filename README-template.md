# Frontend Mentor - Four card feature section solution

This project is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor provides a variety of challenges to help developers practice and improve their coding skills by working on real-world projects. This challenge was a great opportunity to improve my HTML, CSS, and responsive design abilities.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

Here is a screenshot of the project displayed on a desktop screen.

![](./screenshot.jpg)

### Links

- Solution URL: [here](https://your-solution-url.com)
- Live Site URL: [here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- SCSS

### What I learned

**Improving accessibility with semantic HTML**

I gained a deeper understanding of how to improve the accessibility of web pages by using appropriate HTML roles such as `banner`, `presentation` and `contentinfo`. These roles help screen readers and assistive technologies to better understand the structure and purpose of the web page.

**Mastering CSS Grid for Layouts**

One of the most valuable takeaways was learning to use CSS Grid to create responsive and dynamic layouts. For tablet screens, I implemented a simple 2x2 grid structure:

```css
section {  
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;  /* optional */
}
```
I'm leaving out `grid-template-rows: 1fr 1fr;` because the grid will automatically adjust the row heights based on the content. 

For larger screens, I explored a more advanced grid layout that gave me more control over the placement and size of elements:
```css
grid-template-columns: repeat(3, 1fr);  
grid-template-rows: repeat(2, 1fr);  
align-items: center;
```
I refined the layout by strategically positioning individual cards based on their order using `nth-child()` selectors:

- The first card spans two rows.

- The second card automatically takes the next available space in the second column.

- The third card is placed in the second column and second row.

- The fourth card covers two rows and is placed prominently in the third column.

```css
&__card:nth-child(1) {
    grid-row: span 2 / span 2;
}

&__card:nth-child(3) {
    grid-column-start: 2;
    grid-row-start: 2;
}

&__card:nth-child(4) {
    grid-row: span 2 / span 2;
    grid-column-start: 3;
    grid-row-start: 1;
}        
```

This deliberate positioning creates a visually appealing and well-organised grid layout.

### Continued development

I’m planning to dig deeper into creating more complex and flexible layouts by using CSS Grid with SCSS. This means I’ll be:

- Using SCSS features like variables, mixins, and loops to handle repetitive grid patterns more efficiently.
- Experimenting with advanced layout options, like overlapping grid items or grids that change based on the content.
- Making the process of building responsive designs smoother by combining SCSS’s nested structure with CSS Grid’s flexibility.

### Useful resources

- [CSS Grid Layout Guide](https://css-tricks.com/snippets/css/complete-guide-grid/) - This guide has helped me a lot in learning CSS Grid. It explains both the basics and some more advanced features, so I keep coming back to it every time I need to review or learn something new.
- [CSS Grid Generator by Kristjan](https://cssgridgenerator.io/) - I really like this tool because it makes it easy to visually create grid layouts. It's great for trying out different grid structures and quickly getting code snippets. However, it only provides manual settings for individual elements, like `grid-column-start: ` and `grid-row-start:`.
- [CSS Grid Generator by sarah_edo](https://cssgrid-generator.netlify.app/) - This is another cool tool for working with grids. It uses `grid-area` to define where elements go, which I found really interesting and helpful to try out.
- [Layoutit!](https://grid.layoutit.com/) - This is another tool, but focuses `grid-template-areas`, which is a different way of setting up grids and makes it easier to visualise the design.


## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)

