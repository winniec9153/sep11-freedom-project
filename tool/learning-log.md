# Tool Learning Log

## Tool: **P5play**

## Project: **Guess the Number Game**

---

### 09/29/25:
* [P5play](https://p5play.org/learn/sprite?page=0) to learn about sprite
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
### X/X/XX:
* Text


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
