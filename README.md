# Frontend Mentor - Maker pre-launch landing page solution

This is a solution to the [Maker pre-launch landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/maker-prelaunch-landing-page-WVZIJtKLd). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Links](#links)
- [My Process](#my-process)
  - [Built With](#built-with)
  - [What I Learned](#what-i-learned)
  - [Useful Resources](#useful-resources)

## Overview

### The Challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements
- Receive an error message when the form is submitted if:
  - The `Email address` field is empty should show "Oops! Please add your email"
  - The email is not formatted correctly should show "Oops! That doesn’t look like an email address"

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/maker-landing-page-svelte-intersection-observer-css-animations-SJzpmz9mq](https://www.frontendmentor.io/solutions/maker-landing-page-svelte-intersection-observer-css-animations-SJzpmz9mq)
- Live Site URL: [https://fm-maker-landing-page.vercel.app/](https://fm-maker-landing-page.vercel.app/)

## My Process

### Built with
- [Svelte](https://svelte.dev/) 
- [Svelte Intersection Observer](https://github.com/metonym/svelte-intersection-observer)
- CSS Keyframes Animations

### What I Learned

First Svelte project, so I'm sure there's much to be improved upon. Still getting used to component-based structure/development, but so far I like it! The offical Svelte tutorial is fantastic, and I found The Net Ninja's video tutorials (link in Useful Resources) also immensely helpful.

Safari continues to plague me. ~~In this project, the `.invalid` and `focus` styles for the input are not showing up, and I can't figure out why. Any insight into this will be greatly appreciated! The CSS mouse animation also had some serious issues in Safari, so I opted to have the original svg icon be displayed both in Safari and for those who prefer reduced motion.~~

**Edit:** Turns out my Safari was out of date! 😅 Everything works in 15.4 👍 Well, almost. Keyboard tabbing doesn't seem to pick up the maker logo in the header as a link, seemingly skipping it in Safari. The outlines also display oddly on the attribution links when tabbing through them. 🤦‍♀️

### Useful Resources

- [Official Svelte Tutorial](https://svelte.dev/tutorial/basics)
- [Video Tutorial Playlist: The Net Ninja - Svelte Tutorial for Beginners](https://youtube.com/playlist?list=PL4cUxeGkcC9hlbrVO_2QFVqVPhlZmz7tO) 
- [Article: Svelte Transitions and Accessibility](https://geoffrich.net/posts/svelte-summit-2021/)
- [Ryan Mulligan's CSS Site Scroll Micro Animation](https://codepen.io/hexagoncircle/pen/aZWOdE) - Heavily inspired by/blatantly stolen from and lightly tinkered with for the hero.
