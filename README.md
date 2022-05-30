# Pacman Coding Assignment

## Description

This program loops through images in a two dimensional array useing the setTimeout function to schedule execution of a function. The program results in an animated pacman that is chomping away while moving back forth accross the screen.

This repository was created during week 4 of the MIT xPro Professional Certificate in Coding: Full Stack Development with MERN - April 2022

## Installation - Some concepts to help people get started with your project

The boundaries are set using [window.innerwidth](https://developer.mozilla.org/en-US/docs/Web/API/Window/innerWidth).

Use the method [document.getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) to get the first pacman image to show up facing in the correct direction.

[img.style.left](https://www.w3schools.com/jsref/prop_style_left.asp) is used to define to the image location in the x direction.

We a two dimensional array called pacArray. Each array holds two elements. We need to get our function to call the correct elements in the array. The first array is 0, the second array is 1. The first elemnt in each array is [0] and the second element is [1]. The first array forces the direction and the second array forces the mouth open and closed. While going to the right we need to call pacArray[0][0] for moving right with open mouth and the pacmanArray[0][1] for moving right with closed mouth. The direction variable and the focus variable calculate to 0 or 1 in order call the correct image from the array.

The direction variable uses a function checkPageBounds with a conditional [if, then or else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statement that forces direction = 0 when pacman is moving right and direction = 1 when pacman is moving left. Don't forget to account for the image size. Use the CSS [width property](https://developer.mozilla.org/en-US/docs/Web/CSS/width) to define the size of the image.

The focus variable switches between zero and one everyone time the Run function is called. The [modulus operation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder) is used to do this.

The function has to run over and over again in order keep pacman chomping and moving left and right. The built-in javascript function [timeOut()](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) is used to set a timer for how often the function will run.

## Usage - What can you do with this program?

You can use this program to test out some foundational coding concepts.
Image Size - See if you can change the image size.
Initial conditions - What happens if you change the position increment? Can you get pacman to move backwards by changing the filenames?
Animation Speed - Can you change the setTimout argument to make pacman move and chomp faster and slower?
Force variable values to be 0 or 1 using the modulus. This concept can be used to alternate every after every event independant of other conditions.
Force variable values to be 0 or 1 using a conditional statement. This concept can be used to alternate when certain conditiontions related to position are met.

## Support

Mark Dohle
dohle.mark@gmail.com

## Roadmap

Future versions will include ghosts that chase pacman arround and food that pacman has to eat. Pacman eats pellets and runs from the ghosts. The ghosts chase pacman and the pellets appear at random. It is based on [Rabits, Wolves and Carrots](https://github.com/spawnfest/espresso-beam).

## License information

MIT License

Copyright (c) 2020 John Williams

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.






