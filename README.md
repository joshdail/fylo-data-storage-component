# Frontend Mentor - Fylo data storage component solution

This is a solution to the [Fylo data storage component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-data-storage-component-1dZPRbV5n). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS animations
- Flexbox
- Desktop-first workflow

### What I learned

One of the big challenges here was to make the different components of the design display properly on several different screen sizes. I tried to do a decent amount of testing different screen widths and heights to see where different components would break and adjust the design accordingly.

For example, the callout on desktop appears above the meter and on mobile portrait, below the meter. But on mobile landscape, at smaller widths and heights the design would break.

So if the height shrinks, the callout moves below the gauge, and if the width and height both get too small, the callout will disappear so as not to block the two main components.

	@media (height < 380px) {
	  .callout::after {
	    display: none;
	  }
	
	  .callout {
	    top: 65%;
	    left: 50%;
	    width: 40%;
	    translate: -50%;
	    align-items: center;
	  }
	}

	@media (width < 720px) and (height < 450px) {
	  .callout {
	    display: none;
	  }
	}


### Continued development

Even though there is not any real user interaction with this component, I wanted to add in a few accessibility features.

For example, even though the icons do not actually have any function, I made them focusable and added hover states.

I also tried to incorporate some semantic HTML. For example, the icons are enclosed in a menu tag to portray an options menu rather than just being enclosed in a div.

I also added a skip link (which would matter more if there was a navbar at the top, but I added it in for practice).

I added a few animations in as well. I don't consider animations a strong suit of mine by any means, but it was a nice challenge.

### Useful resources

- [MDN web docs: animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation) - This helped me with making sure I understood the options correctly for the CSS animation property. The article on keyframes was also helpful.

## Author

- Github - [github.com/joshdail](https://github.com/joshdail)
- Frontend Mentor - [@joshdail](https://www.frontendmentor.io/profile/joshdail)

