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
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![desktop mode picture](/screenshots/desktop-mode.webp)  
Desktop mode view

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- HTML5 markup languaje
- SASS Languaje
- CSS Flexbox & Grid
- Web-first workflow

### What I learned

At 1st was very dificult to adjust the picture into a div without it overflow its `<div>`, when I could fix it, left side with text couldn't maintain its height, I thought Flexbox was the problem, but I was in a mistake, I could solve this problem using relative height with `vh` unit, this solution look like to code below:

```scss
body {
    height: 100vh;
}
```

After this solution, came other problem, reorder content into left box for mobile-mode. The best solution that I could find, was to use of `@media` to change some properties on the fly, and select wich properties that I needded to change. Flexbox in this case wasn´t better solution, I had to work with grid, and when resolution have to be less than web-mode card width, then grid-template have to change for show elements in diferent order. The code that help me to do this is below:

```scss
{
@media only screen and (max-width: $card-width) {  
	grid-template-columns: 1fr;  
	grid-template-rows: 30% auto;  
	grid-template-areas:  
	    "photo"  
	    "info";  
}
}
```

### Continued development

I want to improve CSS implementation, I am focussed on learn how to use CSS to make animations and better transitions for a pro look.

### Useful resources

- [Complete Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/) - In this page I found a complete guide about CSS Grid. It was helpful for me for complete this challenge.
- [SASS official site](https://sass-lang.com/) - Not much to tell you about this page, there are official documentation about SASS languaje for better CSS coding.
- [Markdown Guide](https://www.markdownguide.org/) - Same that before resource, there are official documentantion and How To guide for using Markdown to make READMER.md file. Maybe this sounds weird, but before this challenge I did not know about Markdown. 

## Author

- Website - [Javier López](http://javierglopezreques.tk/)
- Frontend Mentor - [@jglopezre](https://www.frontendmentor.io/profile/jglopezre)

## Acknowledgments

For about two year I was learning about web development, never, never we feel ready to code, just viewing tutorials and reading a lot of information, it is helpful, but it is not enought. I found Front-End Mentor site while I was looking for information about CSS coding, and I could see a great oportunity for practicing and improve my skills. This, the first challenge was very hard for me to complete, but I could it. I invite you to sign up in the comunity and begin to code, **only doing thing is the way to improve own skills**.

Thank for your work.
