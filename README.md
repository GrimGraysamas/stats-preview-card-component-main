# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

The challenge was to build the following designs into an app.

![Desktop Design](https://apps.stats-card-component.grimfeld.tech/design/desktop-design.jpg)
![Mobile Design](https://apps.stats-card-component.grimfeld.tech/design/mobile-design.jpg)

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshots

![](https://apps.stats-card-component.grimfeld.tech/assets/solution-preview.png)
![](https://apps.stats-card-component.grimfeld.tech/assets/solution-mobile-preview.png)

### Links

- Live Site URL: (https://apps.stats-card-component.grimfeld.tech/)

## My process

### Built with

- HTML5 markup
- [Sass](https://sass-lang.com/)
- Flexbox
- CSS Grid

### Main struggles

- A first issue was to correctly size the width of the two sides of the block. I solved it using _clamp()_ and _calc()_ functions together to avoid using media queries to adapt the width.
  ![](https://apps.stats-card-component.grimfeld.tech/assets/clamp.png)

- A second issue was to colorize the image. In order to achieve this effect I used a block positionned absolutely above the image with a colored background on which I applied filters.
  ![](https://apps.stats-card-component.grimfeld.tech/assets/colorizer.png)
- I solved the change of positionning on mobile by using a combination of flex wrap and order properties on both the content and the image in a media query
  ![](https://apps.stats-card-component.grimfeld.tech/assets/position.png)

### Useful resources

- [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - Very useful article that explains and summarizes the Flexbox with cool assets. Go check it out even if you already master Flexbox

## Author

- Website - [Paul Person aka Grimfeld](https://grimfeld.tech)
- Frontend Mentor - [@GrimGraysamas](https://www.frontendmentor.io/profile/GrimGraysamas)
