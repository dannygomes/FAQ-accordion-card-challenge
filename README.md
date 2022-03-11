# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

## Overview

This challenge was tougher than usual because it had that single box positioned outside of the main card but the corner of the desktop image was cut off from the main card as well. I decided to try and do the added bonus of completeing the challenge with only HTML & CSS.

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Show the answer to a question when the question is clicked

### Screenshot

![](./screenshot.jpg)

### Links

- Live Site URL: [https://peaceful-aryabhata-67494d.netlify.app])

## My process

Started by placing all the HTML that would be needed. 

Divided the card in to two sections, one with the main image, and one with the FAQs. 

Set a custom width on my main element that I though was appropriate and aligned both containers with flex side by side in my main element. 

Had to take the little box image and place it outside of my card div, this was because I needed overflow to be hidden for the desktop image and for the background pattern image but not the little box.

Aligned everything with flexbox and added animations with CSS on the FAQ container questions.



When screen width goes below 900 flex-direction changes to column and all values are updated so everything can align properly.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

I got some more experience using the "position" property in CSS and how to structure my HTML so I can manipulate what properties apply to certain elements.

To start with I used vw on my main element but I then noticed it would be better to used rem as for larger screen sizes the card would stretch out to much. Using a literal value although usually not goot for responsiveness, was better in this case as it kept it more consistent. When the literal value is no longer appropriate for that screen size a media query was used to update it.

Learnt how to use the radio button trick to make a custom animation for the question dropdown effect using the 

Also found a trick searching the web with radio buttons to make the custom dropdown animation. Each radio button has its own label (each FAQ being a label to a radio button) and its display is set to none. This allows me to use the ":checked" selector to display a previously "hidden" element as pressing on the label will check the radio button. So when a label is unchecked, its respective answer-container div has its height set to 0 and overflow to hidden. When a label is checked max height is set and the text shows up. Since only one radio button can be selected at a time only one answer can be displayed at a given moment.

Inially my animation wasn't working the answer would just pop up immediately. I found out this was because for CSS to make a smooth animation it needs a literal initial and final value as referece points. So I could not use "max-heigth: auto" once a label was checked, I had to use a literal value and the animation worked.

## Author

- LinkedIn - [Danny Gomes](https://www.linkedin.com/in/daniel-gomes-80329810a/)
- Frontend Mentor - [@dannygomes](https://www.frontendmentor.io/profile/dannygomes)

## Acknowledgments

Unfortunatelly I can not find the stack overflow post that showed me how to use the radio button trick and the codepen snippet that illustrated how transition will not work without an initial and final value. I apologize, I'll have to do a better job in the future keeping track of my references.
