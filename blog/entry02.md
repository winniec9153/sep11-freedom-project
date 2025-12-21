# Entry 2
##### 12/15/25

### Content: 
I've been learning about [P5play](https://p5play.org/) and the many different functions and elements it have. I learned how to build and customize sprites by changing their size, rotation, color, and images, and how to use groups to effectively control many sprites at once. I also learned about the arrow function property setters, as I learned that they help me randomize and generate a larger number of sprites. Index setters allow me to customize individual sprites within a group. I also learned about [collisions and overlap](https://p5play.org/learn/group?page=2) and how you can detect when sprites touch each other. So bascialy you can check collisions between two sprites, a sprite and a group, or two groups. Callback functions allows it to trigger actions like collecting or deleting an object. I also learned how to add images and sprite images pretty recently through this document on [Sprites with an Image](https://p5play.org/learn/sprite?page=2) from P5Play. So a sprite can have an image by setting sprite.image (or sprite.img). You can set it to: a Q5.Image object, or a URL/file path to an image (like "assets/player.png"). I tinkered with this on [Jsbin](https://jsbin.com/?html,output) creating a cat image:
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
I am currently on the second step of the engineering design process, where I research possible solutions to my problem. So  I noticed that many people struggle with budgeting as they often spend way too much money on unnecessary things and leaving little room for essentials. A solution I came up with was creating this budgeting game using my tool, which is p5play, and creating this interactive website/game that provides a space where you can make good financial decisions. Turning budgeting into a game allows users to learn how to manage money while finding it enjoyable and engaging.

### Skills:
Some skills I developed were consideration and problem decomposition. Consideration had made me think about different perspectives, such as in my day-to-day life, thinking about how it would impact other people, as well as in my game, on how the user would benefit from this budgeting game. This skill is very useful as it encourages me to be more thoughtful and open-minded, making me aware of how my decisions may impact others. Problem decomposition has helped me break down a big task into smaller tasks that are easier to complete. This is important because it helps in many areas, such as schoolwork, where I do it step by step instead of all at once. By this I stay more organized and manage my time better and more effectively with less stress.  
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
