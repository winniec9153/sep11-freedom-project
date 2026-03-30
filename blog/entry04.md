# Entry 4
##### 3/13/26

## Content:
For my Freedom Project, I have been learning how to use p5play throughout the semester, which is a JavaScript library used for making games with sprites and physics. It is very similar to p5.js. So far, I have been focused on understanding the [**World Object**](https://p5play.org/learn/world?page=0) and how it works in p5play. From the documentation, I learned that every p5play project automatically creates a **world object**. This object controls the physics simulation of the game. For example, the world has gravity, which determines how objects move or fall in the game. Gravity has both an **x** and **y value**, meaning that it can affect movement horizontally or vertically. So far, I have made progress toward creating an actual HTML structure of the game/app. I created the main elements, which include the title, balance display, starting money input, and the transaction controls like expenses. This step helped me set up a basic structure, making it easier to build the next features. I also used JS to implement a feature where players can input their starting value, and the app/game will display the player's current balance as it is being stored through [local stroage](https://www.w3schools.com/jsref/prop_win_localstorage.asp).  

Heres is a code snippet of my HTML:
``` HTML
         <!--title of game-->
         <h1> Budget App</h1>
         <!-- the current balance -->
         <h2>Balance: $<span id="balance">0</span></h2>
         <!-- the starting amount -->
         <h3> Start Game</h3>
         <input type="number" id="startingMoney" placeholder="Enter starting money"><button id="startButton"> Start</button>
         <hr>
         <!--Add transaction-->
         <h3> Add Transaction</h3>
         <input type="number" id= "amountInput" placeholder="Enter amount">
         <select id="typeInput">
            <option value="income">Income</option>
            <option value= "expense"> Expense</option>
         </select>
         <button id="addButton"> Add </button>
```
Heres is what I did to save the player's balance:
``` JS
let balance = 0; //creates the balance variable, where player stores their money
            document.querySelector("#startButton").addEventListener("click", function(){ // When the start button is clicked, it will run the code
                var startValue= document.querySelector("#startingMoney").value;//if the player type 500, startValue =500
                balance= Number(startValue); //this convert it into a number. So for example balance=500.
                localStorage.setItem("balance", balance);// this will save the balance by storing the balance in the browser so it wont disapear when the page refreshes.(https://www.w3schools.com/jsref/prop_win_localstorage.asp)
                document.querySelector("#balance").innerHTML=balance; //use to display to balance
            })

```
So this code takes the number the player enters and converts it into a number value, which will be saved to local storage and displayed on the screen.

---

### Engineering Desgin Process:
Right now, I am currently on the 5th of the engineering design process where I will create a prototype. So far I have currently been using HTML and JavaScript to create the HTML structure of the game/app, which includes the title, balance display, and the input area for transactions. Using JS, I am able to add this feature where, when I type in a starting amount, the amount will be saved and the value will be displayed as the player's current balance.
### Skills
While working on my budgeting app/game, I have developed a few skills which I can use outside of this project. One of them includes **problem decomposition**, which means breaking a larger task into smaller, easier, manageable steps. For example, instead of trying to build the entire budgeting game all at once, I broke it into smaller goals with deadlines. This skill is very useful outside of my project because I can apply it to other school assignments and homework. For example, my APUSH study guide has three parts which includes answering HISTORICAL THINKING questions, VOCABULARY, and TEST PRACTICE. This is a lot to do all in one day, so I broke it down by doing Historical Thinking questions for one day, Vocabulary for another day, and the Test Practice for the next day. Another skill I have developed is **debugging**, which involves finding and fixing errors in my code. I have been using this on my SEP homework and classwork assignments. So when my code doesn’t work, I look through each part thoroughly and try to find the cause of the error. I also make sure to comment my code so I will know what each part is for. I also use debugging when doing math; for example, in geometry, when I get a question wrong, I have to look back from the beginning and find the mistake. Both of these skills help me think clearly in my day-to-day life and in my Freedom Project.


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
