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

In addition I learned about [collisions and overlap](https://p5play.org/learn/group?page=2). So you can detect when sprites touch each other 


I also learned about [collisions and overlap](https://p5play.org/learn/group?page=2) and how you can detect when sprites touch each other. So bascialy you can check collisions between two sprites, a sprite and a group, or two groups. Callback functions allows it to trigger actions like collecting or deleting an object.


I also learned how to add images and sprite images pretty recently through this document on [Sprites with an Image](https://p5play.org/learn/sprite?page=2) from P5Play. So a sprite can have an image by setting sprite.image (or sprite.img). You can set it to: a Q5.Image object, or a URL/file path to an image (like "assets/player.png"). I tinkered with this on [Jsbin](https://jsbin.com/?html,output) creating a cat image:
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
So overall, all these learning experiences will help me create a foundation for my budgeting games, such as the background colors and images being added to make it look more appealing.


### Engineering Design Process: 
I am currently on the *second step* of the engineering design process, where I __research the problem__. So in my first blog, I noticed that many people struggle with budgeting as they often spend way too much money on unnecessary things and leaving little room for essentials. I researched someways that I can be able to help with this. So what I came up with was creating this budgeting game using my tool, which is p5play, and creating this interactive website/game that provides a space where you can make good financial decisions. Turning budgeting into a game allows users to learn how to manage money while finding it enjoyable and engaging.

### Skills:
Some skills I developed were **consideration** and **problem decomposition**. When researching about problems people may struggle with when budgetting, it had made me think about different perspectives, such as in my day-to-day life, thinking about how it would impact other people, as well as in my game, on how the user would benefit from this budgeting game. Having consideration is very useful as it encourages me to be more thoughtful and open-minded, making me aware of how my decisions may impact others at school and in my personal life. The skill Problem decomposition has helped me break down a big task into smaller tasks that are easier to complete. This is important because it helps in many areas, such as schoolwork, where I do it step by step instead of all at once. By this I stay more organized and manage my time better and more effectively with less stress.  
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
