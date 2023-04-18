### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces. 

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.
```javascript
const whatToDoForLunch = function(hungry, availableTime) {
  console.log("hungry is", hungry);
  console.log("availableTime is", availableTime);
  if (hungry) {
    if (availableTime < 20) {
      console.log('You don\'t have enough time, pleas pick up a snack or grab something you have ready at home and then get back to work.');
    } else if ((availableTime >= 20) && (availableTime <= 30)) {
      console.log('You\'ve been working hard, so you deserve a break and should take time to cook a tasty meal. Then please don\'t forget to get back to work');
    } else {
      console.log('You\'re in a bootcamp and you should consider how much time You actually have to spare.');
    }
  } else {
    console.log("If you are not hungrey, it's better to get back to work and wait until you are hungry!");
  }
};

console.log("I'm hungry and I have 20 minutes for lunch.");
whatToDoForLunch(true, 20);
console.log("---");

console.log("I'm hungry and I have 50 minutes for lunch.");
whatToDoForLunch(true, 50);
console.log("---");

console.log("I'm not hungry and I have 30 minutes for lunch.");
whatToDoForLunch(false, 30);
console.log("---");

console.log("I'm hungry and I have 15 minutes for lunch.");
whatToDoForLunch(true, 15);
```