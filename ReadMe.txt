JavaScript / HTML / CSS

Process

- Played around in the console on my web browser and used the transform features to move the various hand elements at certain degrees.
- Searched web documents on how to select a specific DOM element. I was going to start working on the seconds hand of the clock first.
- Attempted to use various functions to get the seconds hand to move, but none of them worked.
- Two attempts at moving the hands of the clock can be seen within the HTML document as a comment.
- I was able to select and change the behavior of the <div> classes using document.querySelector().style.transform
- I was then able to select and rotate each individual hand.

Some notes...

- There are three divs, one for each hand of the clock.
- The transform-origin under .hand in the CSS is at 100%, which allows the hands to pivot around the center instead of pivoting on themselves.
- The transform: rotate under .hand in the CSS is at 90 degrees, which allows the hands to begin at 12 o'clock.
- Each function within the script tags allows the hands to move according to the local time. 
- For my functions, I use getSeconds, getMinutes, and getHours. I then create a constant for each respective function that equals the amount of degrees I want the hand to move. 
- The div element can then be accessed by  inserting the above mentioned constant within style.transform
	- Here is an example for the hours hand:
	    function setDate3 () {
	 	const now = new Date();
	       	const hours = now.getHours();
	       	const hoursDegrees = ((hours / 12) * 360) + 90;
	       	hoursHand.style.transform = `rotate(${hoursDegrees}deg)`; 
	    }
- This clock was a part of the JavaScript 30 lessons by Wes Bos, which provided the CSS.
