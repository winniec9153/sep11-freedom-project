# Tool Learning Log

## Tool: **P5play**

## Project: **Budjeting Game**

---

### 09/29/25:
* [P5play](https://p5play.org/learn/sprite?page=0) to learn about sprite(Basic Properties)
* sprite refers to an object, character, or background that can move
  *   So we are able to change its position, length, width, size and shape.
  *   `new Sprite()` constructor create a new sprite object
    * it contains varaibles that define its size, position and appearances.
* Examples:
  * we can change the width and height of the sprite through `sprite. width= ;` and ` sprite.height= ;`.
  * We can also do sprite roations(`sprite.rotation= ;` which will rotate the spirte( I rotated it by 45 degrees)
  * we can aslo change its color and outside stroke. The stroke is like a border color. (I made mine red and the sprite pink).
 ``` JS
  let sprite;
function setup() {
	new Canvas(238, 100);
	sprite = new Sprite();
	sprite.width = 90;
	sprite.height = 50;
  sprite.rotation = 45;
  sprite.color = 'pink';
  sprite.stroke = 'red';
}
function update() {
	clear();
}
```
* I also tried the challenge on converting the green box into a blue circle with a diameter of 30. At first I did it wrong as i did `sprite.color= 'blue';` and `sprite.diameter= 30;`. I forgot to change the `sprite` to `ball` which cause a little error. So once I changed it, the ball appeared. Next time I will try on making more shaped and maybe try making a character with these shapes.
``` JS
let ball;
function setup() {
	new Canvas(200, 256);
	ball = new Sprite();
	// write your code here!
	ball.color= 'blue';
  ball.diameter= 30;
}
function update() {
	clear();
}
```

### 10/27/25:
* [P5play-group](https://p5play.org/learn/group?page=0) to learn about Groups(Soft and Dynamic Inheritance)
* A collection of and a blueprint for sprites with similar traits and behaviors.
   * Examples: the dots in Pac Man
* You can check how many sprite is in a group through `group.length`.
 * You can access sprite in groups through indexs, as indexs are arrays
	 * In an array it start with 0, not 1.
     * 	Example:
     * 	``` JS
        dots[5].color = 'green';
        ```
        this shows:
       	<img width="720" height="66" alt="image" src="https://github.com/user-attachments/assets/33389ff4-8329-409a-a5a2-375423d63f06" />
* You can change all the sprite property in a group:
   ``` js
   dots.color = 'green';
   ```
	* this makes all the dots green.
* You can also move all the sprites all at once through the `moveToward` funtion which is really cool(movement funtion).
	* Example of that code:
   ``` JS
   dots.moveTowards(mouse);
   ```
   * This makes all the dots move where my arrow goes.
* Something I will try next is combining the stuff I learned about sprites and groups all together.

### 11/10/25:
* [P5play-group](https://p5play.org/learn/group?page=1) to learn about Arrow setters
* Arrow Function Property Setters
    * it assigns a group proerty to an arrow so that means eachtime a new sprite is created in the group. Forexample instead of putting in a specific value each time( group.x=100), you can create alot and randomize the values.
    * `group.x = () => random(width)`
    * This Property `group.amount` can control how much sprite you want in a group.
      * Forexample if I put `gem.amount=1000` then there will be 1000 gem/sprite being genreated.
      * SO if we put everything together you would get this:
    ``` JS
    let gems = new Group();
    gems.amount = 1000;
    gems.x = () => random(width);
    gems.y = () => random(height);
    ```
      * This will have 1000 sprites/gems in all different locations on the canvas
* Indexed arrow function setters
  * you an use an arrow function to set a property for every sprite in a group, and the index `i` lets you customize each sprite individually.
  * An example of me trying this:
``` JS
  let balls;

function setup() {
  createCanvas(400, 200);
  balls = new Group();

  for (let i = 0; i < 5; i++) {
    let ball = createSprite(0, 100, 30, 30);
    balls.add(ball);
  }
  balls.forEach((sprite, i) => sprite.position.x = 50 + i * 60);
}
function draw() {
  background(220);
  drawSprites();
}
```
  * So 5 balls will appear in a row, and each ball is the same vertical position (y=100). So `for (let i = 0; i < 5; i++) { ... }` loops 5 time to create 5 sprite balls.
* Relazing group.amount can gernate lots of sprites was a big A-Ha momment for me.
* Question I still have is are there any limit for my much sprite I can use?
* Next thing I will try is to try conbine group.amount with indexed arrow setter.

### 11/17/25:
* Collisions and Overlaps on [P5play-group](https://p5play.org/learn/group?page=2)
  * Collisions and overlaps let you detect when sprites touch each other. You can check collisions between two sprites, a sprite and a group, or two groups.
 * Some functions you can use are:
 	* collides, colliding, collided
 	* overlaps, overlapping, overlapped
* Instead of just using these in if statements, you can give them a callback function. The callback runs automatically when the collision or overlap happens and gives you the two sprites that touched.
	* For example, if a player sprite overlaps a gem in a group, the callback function can collect or delete the gem.
 * I tried tinkering with the code through experimenting with random colors for gems, tweaking the movement speed for the player and added rotation before deleting gems just to see the effect.
 * Code of it :
```JS
let player, gems;
function setup() {
  new Canvas(160, 456);

  // This create a group of gems with random properties
  gems = new Group();
  gems.diameter = 10;
  gems.x = () => random(0, canvas.w);
  gems.y = () => random(0, canvas.h);
  gems.color = () => color(random(255), random(255), random(255)); // random gem colors
  gems.amount = 80;

  player = new Sprite();
  player.color = "orange";
  player.diameter = 20;

  // Collect gems when player overlaps
  player.overlaps(gems, collect);
}

function collect(player, gem) {
  gem.rotation = random(360); // a rotation before deleting
  gem.delete();
}

function update() {
  clear();
  player.moveTowards(mouse, 5); // this added speed value to tinker with movement
}
```
* My a-ha moment was learning that I could use arrow functions to randomize properties like` x`,` y`, and color for all sprites in a group.
* I’m curious if there is a limit to how many sprites I can generate at once without crashing the game.
* Next time I will try combining groups, arrow function setters, and collision effects.


### 12/4/25:
* Sprites with an Image on [P5play-sprite](https://p5play.org/learn/sprite?page=2)
* 1. Using Images on Sprites
	* A sprite can have an image by setting sprite.image (or sprite.img).
 	* You can set it to:
  		* a Q5.Image object, OR
    	* a URL/file path to an image (like "assets/player.png").
     * Loading Images BEFORE the Program Starts
* 2. If your game needs images ready before setup runs, use:
     ``` JS
     function preload() {
     	myImage = loadImage("path/to/image.png");
     } 
```
* This is so your game doesn’t try to draw a sprite before the image is loaded (prevents errors or blank images).
* 3.Offsetting the Sprite Image
	* You can shift the image relative to the sprite’s center using:
``` JS
sprite.image.offset.x
sprite.image.offset.y
```
* Why use offset???
	* Because it helps align the picture with the sprite’s physics collider (the “hitbox”).
 	* Useful if the image's visual center doesn’t match the sprite’s physics center.
Example of this all being used:
``` JS
let monster;

function setup() {
	new Canvas(500, 120);
	monster = new Sprite();
	monster.diameter = 70;
	monster.image = 'assets/monster.webp';
	monster.image.offset.y = 6;
}
function update() {
	clear();
	monster.debug = mouse.pressing();
}
``` this creates a monster image.
* I created a code with a different image:
``` JS
let cat;

function setup() {
  new Canvas(500, 120);

  cat = new Sprite();
  cat.diameter = 70;
  cat.image = 'assets/cat.webp';
  cat.image.offset.y = 6;
}

function update() {
  clear();
  cat.debug = mouse.pressing();
}
```
So by me doing this, it creates a cat image. 


### 12/15/25:

* Sprites with an Image on [P5play-sprite](https://p5play.org/learn/sprite?page=2)
* 1. Using Images on Sprites
	* A sprite can have an image by setting sprite.image (or sprite.img).
 	* You can set it to:
  		* a Q5.Image object, OR
    	* a URL/file path to an image (like "assets/player.png").
     * Loading Images BEFORE the Program Starts
* 2. If your game needs images ready before setup runs, use:
     ``` JS
     function preload() {
     	myImage = loadImage("path/to/image.png");
     }

     
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
