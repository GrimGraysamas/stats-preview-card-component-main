# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [Process](#process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshots

<div style="display: flex; align-items: center; justify-content: space-between">
  <img src="https://apps.stats-card-component.grimfeld.tech/assets/solution-preview.png" width="75%">
  <img src="https://apps.stats-card-component.grimfeld.tech/assets/solution-mobile-preview.png" width="24%">
</div>

### Links

- [Live Demo](https://apps.stats-card-component.grimfeld.tech/)

## Process

### Built with

- HTML5 markup
- [Sass](https://sass-lang.com/)
- Flexbox
- CSS Grid

### Main struggles and their solutions

- A first issue was to correctly size the width of the two sides of the block. I solved it using _clamp()_ and _calc()_ functions together to avoid using media queries to adapt the width.

  ```sass
    .content
      width: clamp(calc(375px - 8rem), calc(50% - 8rem), 40ch)
      // 8rem being the total padding of the .content
  ```

- A second issue was to colorize the image. In order to achieve this effect I used a block positionned absolutely above the image with a colored background on which I applied filters.

  ```sass
    .image-wrapper
      width: clamp(375px, 100%, 50%)
      position: relative
      .color
        position: absolute
        width: 100%
        height: 100%
        background-color: hsla(277, 64%, 61%, 0.6)
        filter: saturate(150%) contrast(200%) brightness(50%)
      img
        width: 100%
        height: 100%
        object-fit: cover
  ```

- I solved the change of positionning on mobile by using a combination of flex wrap and order properties on both the content and the image in a media query
  ```sass
    .main
      display: flex
      flex-wrap: wrap
    @media all and (max-width: 1024px)
      .content
        order: 2
      .image-wrapper
        order: 1
  ```

### Useful resources

- [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - Very useful article that explains and summarizes the Flexbox with cool assets. Go check it out even if you already master Flexbox

## Author

- Website - [Paul Person aka Grimfeld](https://grimfeld.tech)
- Frontend Mentor - [@GrimGraysamas](https://www.frontendmentor.io/profile/GrimGraysamas)
