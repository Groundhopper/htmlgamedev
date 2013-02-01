005 Kick the ball
===================================

Now that we have introduced rooney the greatest striker in the world into
our gaelic game.  We also allowed an english player blast penalties over
the box which they like doing under pressure.  Rooney is also taking 
the right run up and he is a left footer player and we even see him
make the kick motion.  Well its now time to see the ball move
 
Aim
---------
* Another look at functions
* Understanding where you need to put functions


Game aim
-----------
* Make the ball move

Ok so lets get started.

Make the ball move
------------

When rooney kicks the ball needs to move right! so its time to immediately
make the ball move so we will create a function called moveBall.  Lest
create the function

````javascript
function moveBall() {
	
}
````

Now that this function has been created, where do we need to call it from?
Think about where does the ball need to move? Where did rooney kick the ball
and the ball? Remember the function that changed the image? Was it called

We need to add it after the rooneyKickBall function which was
triggered in the rooneyRun function

````javascript
function rooneyRun() {
	var ballPosition = 200;
	
	var rooneyPosition = parseInt(rooney.css('left'));
	if(ballPosition < (rooneyPosition)) {
		rooney.css('left',(rooneyPosition-5)+'px');
		setTimeout(rooneyRun,50);
	} else {
		rooneyKickBall();
		moveBall();
	}
}
````

Now that the function is called, time to start writing some code.  Lets
get started with making the ball move.  To gets started we need
 to get the ball top value, how do we get top value for the ball?
 
* First we get the variable name ball
* So its ball.
* Need to get the top value ball.css('top')
* This returns a pixel value with px
* We need a number to use

The following code creates a variable with the current top value

````javascript
function moveBall() {	
	var currentTop = parseInt(ball.css('top'));
	
}

````