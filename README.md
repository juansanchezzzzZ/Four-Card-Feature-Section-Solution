# Frontend Mentor - Four Card Feature Section Solution

<div align="center">

![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![NEWBIE](https://img.shields.io/badge/Frontend_Mentor-NEWBIE-3DB8FF?style=for-the-badge)

</div>

A responsive feature section built as part of a Frontend Mentor challenge.

This project focuses on Flexbox layouts, responsive design, card positioning, typography, shadows, and creating a clean and scalable component-based layout.

---

## Preview

![Design preview for the Four Card Feature Section](./design/desktop-preview.jpg)

---

## Live Demo

- Live Site: https://juansanchezzzzz.github.io/Four-Card-Feature-Section/
- Frontend Mentor Challenge: https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK

---

# Overview

This project recreates the Four Card Feature Section design provided by Frontend Mentor.

The main objectives were:

- Semantic HTML5 structure
- Responsive layouts
- Flexbox positioning
- Card alignment
- Responsive typography
- CSS shadows
- CSS positioning
- Layout organization
- Mobile adaptation
- Clean CSS architecture

---

# Challenges Faced

## Understanding Full Height Layouts

One of the first concepts I reinforced during this project was creating a layout that fills the entire viewport while keeping the footer at the bottom.

```css
body{
    min-height: 100dvh;
    display: flex;
    flex-direction: column;
}

main{
    flex: 1;
}
```

This helped me better understand how Flexbox can be used for page-level layouts and how elements can automatically occupy remaining space.

---

## Learning the Difference Between `vh` and `dvh`

While working on the page layout, I learned the difference between:

```css
100vh
```

and

```css
100dvh
```

I discovered that `dvh` represents the actual visible viewport height and adapts dynamically when browser UI elements appear or disappear on mobile devices.

---

## Centering Text While Limiting Line Length

The introductory paragraph needed to remain centered while preventing lines from becoming excessively long.

```css
p{
    max-width: 55ch;
    margin-inline: auto;
}
```

This improved my understanding of content width management and typography best practices.

---

## Creating Different Card Accent Colors

Each card required its own colored top border.

```css
.card--cyan{
    border-top-color: var(--Cyan);
}
```

This reinforced the importance of reusable and scalable CSS architecture.

---

## Reproducing the Card Shadows

One of the visual details that required careful attention was the subtle shadow effect beneath each card.

```css
box-shadow: 0 15px 30px rgba(131, 166, 210, 0.2);
```

Through this process I gained a better understanding of:

- Shadow offsets
- Blur radius
- Opacity
- Visual depth
- Modern UI styling

---

## Positioning Icons Inside the Cards

The card icons needed to appear in the bottom-right corner of each card.

```css
.card{
    position: relative;
}

.card img{
    position: absolute;
    right: 1.5rem;
    bottom: 1.5rem;
}
```

This challenge strengthened my understanding of positioning contexts and how absolutely positioned elements interact with their nearest positioned ancestor.

---

## Understanding Responsive Layout Changes

The desktop design uses a horizontal card arrangement, while the mobile version stacks all cards vertically.

```css
@media (max-width: 50rem){
    .cards-section{
        flex-direction: column;
    }
}
```

This helped me gain more experience with responsive design and mobile-first thinking.

---

## Creating Responsive Typography

The main heading looked too large on smaller devices.

```css
@media (max-width: 50rem){
    .main-title{
        font-size: 1.5rem;
        line-height: 1.4;
    }
}
```

This improved both readability and visual balance across screen sizes.

---

## Avoiding Overly Generic Selectors

Initially I styled all headings using:

```css
h1{
    ...
}
```

However, I later realized that the cards also contained headings, causing unintended styling conflicts.

```css
.main-title{
    ...
}
```

This taught me the importance of using specific selectors to avoid side effects as projects grow.

---

## Structuring Cards with Flexbox

To organize content inside each card, I used:

```css
.card{
    display: flex;
    flex-direction: column;
}
```

This allowed elements to stack naturally and made future positioning much easier.

---

## Debugging Small HTML Errors

During development, I encountered an issue where the stylesheet was not loading correctly.

```html
<link rel="stylesshet" href="styles.css">
```

instead of:

```html
<link rel="stylesheet" href="styles.css">
```

This reminded me how important it is to inspect HTML carefully when debugging.

---

# Built With

- HTML5
- CSS3
- Flexbox
- CSS Custom Properties
- Media Queries
- CSS Positioning
- Box Shadows
- Responsive Design
- Semantic HTML

---

# What I Learned

Through this project I gained more experience with:

- Building responsive layouts with Flexbox
- Creating full-height page layouts
- Using `100dvh` effectively
- Understanding the differences between `vh` and `dvh`
- Structuring pages using Flexbox
- Keeping footers pinned to the bottom
- Managing content width with `max-width`
- Centering content using `margin-inline: auto`
- Creating reusable CSS modifier classes
- Styling cards with accent colors
- Building soft modern shadows
- Using `box-shadow` effectively
- Working with relative and absolute positioning
- Positioning icons inside components
- Creating responsive typography
- Using media queries for layout adjustments
- Avoiding overly generic CSS selectors
- Organizing components with Flexbox
- Debugging HTML and CSS issues
- Improving CSS maintainability
- Building cleaner and more scalable stylesheets

---

# Future Improvements

If I were to rebuild this project, I would:

- Start with a mobile-first approach
- Create more reusable utility classes
- Further improve spacing consistency
- Explore CSS Grid as an alternative layout solution
- Refine card sizing for intermediate breakpoints
- Improve accessibility and semantic structure

---

# Author

- Frontend Mentor - https://www.frontendmentor.io/profile/juansanchezzzzz
- GitHub - https://github.com/juansanchezzzzz
