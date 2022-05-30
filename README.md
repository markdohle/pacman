# pacman.github.io
Sit back relax and watch Pacman go back and forth

This is program rotates through images in an array and results in pacman chomping away while moving back forth accross the screen. The boundaries are set using [window.innerwidth](https://developer.mozilla.org/en-US/docs/Web/API/Window/innerWidth).

Use the method [document.getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) to get the first pacman image to show up facing in the correct direction.

[img.style.left](https://www.w3schools.com/jsref/prop_style_left.asp) is used to define to the image location in the x direction.

We a two dimensional array called pacmanArray. Each array holds two elements. We need to get our function to call the correct elements in the array. The first array is 0, the second array is 1. The first elemnt in each array is [0] and the second element is [1]. The first array forces the direction and the second array forces the mouth open and closed. While going to the right we need to call pacmanArray[0][0] for moving right with open mouth and the pacmanArray[0][1] for moving right with closed mouth. The direction variable and the focus variable calculate to 0 or 1 in order call the correct image from the array.

The direction variable uses a function checkPageBounds with a conditional [if, then or else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statement that forces direction = 0 when pacman is moving right and direction = 1 when pacman is moving left. Don't forget to account for the image size. Use the CSS [width property](https://developer.mozilla.org/en-US/docs/Web/CSS/width) to define the size of the image.

The focus variable switches between zero and one everyone time the Run function is called. The [modulus operation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder) is used to do this.

The function has to run over and over again in order keep pacman chomping and moving left and right. The built-in javascript function [timeOut()](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) is used to set a timer for how often the function will run.

This repository was created during week 4 of the MIT xPro Professional Certificate in Coding: Full Stack Development with MERN - April 2022
