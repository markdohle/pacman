# pacman.github.io
Sit back relax and watch Pacman go back and forth

This is program rotates through images in an array and results in pacman chomping away while moving back forth accross the screen. The boundaries are set useing [window.innerwidth](https://developer.mozilla.org/en-US/docs/Web/API/Window/innerWidth).

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
