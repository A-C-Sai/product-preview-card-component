# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

Building a Product preview card component using HTML5 and CSS3.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![Solution Mobile Verion](./images/Solution-Mobile-Layout.png)
![Solution Desktop Verion](./images/Solution-Desktop-Layout.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/A-C-Sai/product-preview-card-component)
- Live Site URL: [Add live site URL here](https://a-c-sai.github.io/product-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

I wasn't sure on how to change the product preview image from mobile to desktop version automatically, after researching on I found out that I could declare a img without the src attribute in HTML and use the content property in CSS to set the image. This allowed me to change the image via CSS automatically in the media query as all I needed to do was change the file path to a different image when the viewport width changes. Although this works i've read that this is not that best practice. Anyone know any alternative solutions?

- ![stackoverflow link](https://stackoverflow.com/questions/2182716/is-it-possible-to-set-the-equivalent-of-a-src-attribute-of-an-img-tag-in-css)

```html
<div class="preview">
  <img class="preview-img" alt="product preview" />
</div>
```

```css
.preview-img {
  content: url("./images/image-product-mobile.jpg");
}
```

```css
@media screen and (min-width: 1140px) {
  .preview-img {
    content: url("./images/image-product-desktop.jpg");
  }
}
```

### Continued development

- I experimented a lot with widths and max-width to get the correct sizing and layout as you will see in my CSS file, not sure if this is the right approach.
- Though I was able to use flexbox I am still experimenting with the different flex properties before I land on the correct one. I find flex-grow/shrink and basis the most tricky.
- This was technically my first time attempting a responsive layout and i'm not sure if I approaced or if my coding practices are correcct.

## Author

- Frontend Mentor - [@A-C-Sai](https://www.frontendmentor.io/profile/A-C-Sai)
