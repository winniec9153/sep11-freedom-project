# Entry 3
##### 02/02/26

## Content:
I have been learning my tool by watching YouTube tutorials and going through the [document tutorials](https://p5play.org/learn/sprite?page=0). Over winter break, my goal was to learn more advanced features of p5play and use them in my budgeting game. I watched YouTube videos and experimented on Jsbin to practice adding animations and effects, like sparks and smooth movements. This helped me see how to make my sprites and interactions more interesting. After winter break, I started using what I learned by combining sprite groups, collisions, and images into one interactive sketch. This shows I am moving from just experimenting to slowly start building a real game prototype based on my freedom project idea. 

For example, I used arrow function property setters and index setters to control a group of circles:
``` JS
let circle;

function setup() {
  createCanvas(200, 200);
  
  circle = new Group();
  circle.x = () => random(width);
  circle.y = () => random(height);
  circle.diameter = 15;
  circle.color = 'white';
  
  circle.amount = 10;
  circle[0].color = 'yellow';
  circle[0].diameter = 30;
}
``` 
So all the circles are white and are located in different positions, but one of the circles is bigger and yellow due to the index setters. Another thing i practices using this [article of sprite](https://p5play.org/docs/Sprite?utm_source=chatgpt.com) to learn, was overlaps and callback functions to make interactions:
Example code:
```Js
player.overlaps(stars, catchStar);

function catchStar(player, star) {
  star.x = random(width);
  star.y = random(-50, 0);
}
```
This code moves the star to a new random position whenever the player touches it.
. 
Something I also experimented with was adding images to sprites which I learned from reading [p5js documentation](https://p5play.org/learn/sprite?page=2):
```
let cat;

function setup() {
  createCanvas(500, 120);
  cat = new Sprite();
  cat.diameter = 70;
  cat.image = 'assets/cat.webp';
}
```
So what i want to learn next is mostly trying to focus on combining everyhing I have learned into a complete budgetting game. i want to test out everything over again to see how I will be able to use for what I want to include in my budgeting game. So what I had plan so far to include is adding game mechanics such as tracking money , impove interactivity trhough adding keyboard controls, and enhacinging visuals which I learned how to do already. So I will learn on how to add keyboard control and a way to track money using p5js.



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
