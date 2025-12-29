# Entry 2
##### 12/15/25

### Content: 
I've been learning about [P5play](https://p5play.org/) and the many different functions and elements it have. Through reading documentation and tinkering, I learned how to build and customize sprite by changing their size, roatation, coolor and images. I also learned how to use group to effecrively control many sprite at once.
An important concept I learned was **arrow function property setters** which can help me randomize and generate a large number of sprite quickly. I also learned about **index setters**, which allows me to customize individual sprites within a group intead of changing all of them at once. An example of **arrow function property setter** and **index setters** combine is this:  
``` JS
let circle;
function setup() {
  new Canvas(200, 200);

  circle = new Group();

  circle.x = () => random(width);
  circle.y = () => random(height);
  circle.diameter = 15;
  circle.color = 'white';

  stars.amount = 10;
  circle[0].color = 'yellow';
  circle[0].diameter = 30;
}
```  
So all the circles get random positions and are the color white and through index setter one of the circle will become yellow and bigger while the rest stays the same.

In addition I learned about [collisions and overlap](https://p5play.org/learn/group?page=2) in P5play. So you can detect when sprites touch each other whether it is between two individual sprites, a sprite and a group, or two groups. I also learned how callback functions can be used to trigger actions, such as collecting or deleting an object.
So when I was tinkering `player.overlaps(stars, catchStar);` this line is what check for overlap as the `player` is the sprite doing the checking, the `stars` is the group being checked, and the `overlap()` is what detect when sprite touch. 
```JS
function catchStar(player, star) {
  star.y = random(-50, 0);
  star.x = random(canvas.w);
}
```
So this function is the **callback** and it runs when an overlap happens. 


I also learned how to add images and sprite images pretty recently through this document on [Sprites with an Image](https://p5play.org/learn/sprite?page=2) from P5Play. So a sprite can have an image by setting sprite.image (or sprite.img). You can set it to: a **Q5.Image object**, or a ((URL/file path** to an image (like "assets/player.png"). I tinkered with this on [Jsbin](https://jsbin.com/?html,output) creating a cat image:
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
So overall, all these learning experiences will help me create a foundation for my budgeting games. Knowing how to add background colors, images, and interactive spirtes  will make it look more appealing and engaging to the users. 

My Freedom Project goal/plan for the winter break is to watch additional videos on youtube as well as tinkering with my tool on Jsbin. I plan on doing some more research on Subgroups and keep track of my learning in my learning log.


### Engineering Design Process: 
I am currently on the *second step* of the engineering design process, where I __research the problem__. So in my first blog, I noticed that many people struggle with budgeting as they often spend way too much money on unnecessary things and leaving little room for essentials. I researched someways that I can be able to help with this. So what I came up with was creating this budgeting game using my tool, which is p5play, and creating this interactive website/game that provides a space where you can make good financial decisions. Turning budgeting into a game allows users to learn how to manage money while finding it enjoyable and engaging.

### Skills:
---
#### Consideration

When researching about problems people may struggle with when budgetting, it had made me think about different perspectives, such as in my day-to-day life, thinking about how it would impact other people, as well as in my game, on how the user would benefit from this budgeting game. Having consideration is very useful as it encourages me to be more thoughtful and open-minded, making me aware of how my decisions may impact others as well as my self at school and in my personal life. An example of consideration in my life is when I 
share my notes with a classmate who was absent because I am thinking about how missing class could affect them and I want to help them stay on track instead of falling behind. I understand how being absent may make you fall behind and with the help of classmate notes, it will be able to help me catch up faster.

---
#### Problem Decomposition
The skill of problem decomposition has helped me break down a big task into smaller tasks that are easier to complete. This is important because it helps in many areas, such as schoolwork, where I do it step by step instead of all at once. It helps me stay organized, reduces stress by not doing everything at once, makes it easier to track all my progress, and is very useful for school, projects (Freedom Project), and personal tasks. For example, I have a midterm exam for chemistry coming up, and I am breaking up everything I learned into different sections to make studying more efficient.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
