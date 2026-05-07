# Presentation Plan

## Hook
* A statisitic of budgetting
  *  Did you know that 31% of teens have a budget and follow it carefully, while another 30% have a budget but don’t follow it consistently.


## Product
* I will present my Budgeting App and how it works through me demoing how I would use this Budget App through out the day.
## Process
* I will show my code from my MVP like the main stuff and then show how I added my Beyong MVP which is me adding background color and using p5play to make it better.
 * Code snippet from MVP:
  ``` JS
   var balance = 0; //creates the balance variable, where player stores their money
            var categories = {
                Food: 0,
                Gas: 0,
                Entertainment: 0,
                Other: 0
            };
            // a new function for categories
             function updateCategories(){ //updates the list on your screen so every time you add a transaction, this function refreshes the category totals display

                var list = document.querySelector("#categoryTotals");
                list.innerHTML = ""; //This clears the list first so it doesn’t stack duplicates

                for(var cat in categories){ //Go through every key (Food, Gas, Entertainment, Other) inside the categories object one by one.
                    var li = document.createElement("li"); //Creates a new list item
                    li.innerHTML = cat + ": $" + categories[cat];//Fills it with text, for example  it will be like: Food: $50, cat = "Food" categories[cat] = 50
                list.appendChild(li);
                }
            }
   ```
* Code snippet from Beyond MVP
```JS
 p.draw = function () {
                p.clear(); // transparent background so lightblue body shows through

                for (var i = 0; i < signs.length; i++) {
                    var s = signs[i];

                    // move upward with a gentle side wobble
                    s.wobble += s.wobbleSpeed;
                    s.x += s.speedX + Math.sin(s.wobble) * 0.5;
                    s.y += s.speedY;

                    // reset to bottom when it floats off the top
                    if (s.y < -60) {
                        signs[i] = createSign(p);
                        signs[i].y = p.height + 20; // start from bottom
                    }
```

## Conclusion
* I will say how overall Budgeting app are very beneficial and will help you fianncially so you dont over spend and realise how much money you are spednig. Then I will say a take away I had when making this Budgeting App.
*  

<!-- EXAMPLE

## Hook
* Verbal riddle of GGD

## Product
* GIF/Demo of example/non-example

## Process
* Flowchart of plan
  * MVP: noun -> door -> yes/no
  * Beyond MVP: noun -> word relation API -> noun API -> yes/no, with counterexample
* Code snippets of:
  * MVP
  * Both APIs
  * Challenge with API keys

## Conclusion
* [URL to project]
* Takeaways
  * Less = more: the heart of the riddle was one line of code; it obviously took more to make the entire thing work, but one complicated line of regular expressions was essentially the solution to the riddle
  * Expect the unexpected: it’s important to budget time for things you don’t account for; for example, I didn’t consider the fact that I would need another entire API to detect nouns
  * Determination is key: ironically enough, I had to make my API keys private. At first, it didn’t seem like it was possible, which meant I couldn’t publish my app. But after all of that hard work, I was determined to find a solution, and I found it in config variables.
* "Presentation can’t, but a speech can"


-->
