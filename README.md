# pacman.github.io
Sit back relax and watch Pacman go back and forth

This is program rotates through images in an array and results in pacman chomping away while moving back forth accross the screen. The boundaries are set useing [window.innerwidth](https://developer.mozilla.org/en-US/docs/Web/API/Window/innerWidth).

Use the method [document.getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) to get the first pacman image to show up facing in the correct direction.

Use the CSS [width proterty](https://developer.mozilla.org/en-US/docs/Web/CSS/width) to define the size of the image.

We a two dimensional array called pacmanArray. Each array holds two elements. We need to get our function to call the correct elements in the array. The first array is 0, the second array is 1. The first elemnt in each array is [0] and the second element is [1]. The first array forces the direction and the second array forces the mouth open and closed. While going to the right we need to call pacmanArray[0][0] for moving right with open mouth and the pacmanArray[0][1] for moving right with closed mouth. The direction variable and the focus variable calculate to 0 or 1 in order call the correct image from the array.

The direction variable uses a function with a conditional [if, then or else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statement that forces direction = 0 when pacman is moving right and direction = 1 when pacman is moving left.

The focus variable switches between zero and one everyone time the Run function is called. The [modulous operation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder) is used to do this. 

The function Run() 

function Run() {
        let img = document.getElementById("PacMan");
        let imgWidth = img.width
        focus = (focus + 1) % 2;
        direction = checkPageBounds(direction, imgWidth);
        img.src = pacArray[direction][focus];
        if (direction) {
            pos -= 20;
            img.style.left = pos + "px";
        } else {
            pos += 20;
            img.style.left = pos + 'px';
        }
        // Use setTimeout to call Run every 200 millesecs
        setTimeout(Run,200)
    }

    function checkPageBounds(direction, imgWidth) {
        //
        // Complete this to reverse direction on hitting page bounds
        // 
        if ( direction === 0 && pos + imgWidth > Xmax) {
            direction = 1
        } else if  (direction === 1 && pos < 0) {
            direction = 0
        }

        return direction;
    }
</SCRIPT>

<body>
    <img id="PacMan" src="PacMan1.png" width='200' onclick="Run()" style="position:absolute"> </img>
</body>
