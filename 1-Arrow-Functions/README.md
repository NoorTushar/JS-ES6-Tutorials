# Arrow Functions

```js
//traditional function
function sum(a, b) {
  return a + b;
}
console.log(sum(5, 7));

//arrow function
const sum2 = (a, b) => {
  return a + b;
};
console.log(sum2(5, 7));

//if you have one parameter and also one like of execution, you can shorten the code like below:
const greet = (user) => user;

//here note that we did not use () as well as we did not use the 'return' keyword as well

/* ---------------------------------------------- */

//Let us see the main use of arrow function with 'this' keyword

let person = {
  name: "Tushar",
  age: 19,
  address: "Eskaton",
  hobbies: ["reading", "coding", "gaming"],
  showName() {
    this.hobbies.forEach((item) => console.log(item));
  },
};
person.showName(); //output: "reading", "coding", "gaming"

//Arrow Functions with ForEach loop

let myArray = ["apple", "orange", "coconut"];

//traditional way:
myArray.forEach(function (item) {
  console.log(item);
});

//using arrow function
myArray.forEach((item) => console.log(item));

//also
myArray.forEach((item, index) => {
  console.log(`Item is: ${item}`);
  console.log(`at index: ${index}`);
});

//Arrow Functions with SetTimeout()

//using traditional way
setTimeout(function () {
  console.log(`traditional way`);
}, 2000);

//using arrow function
setTimeout(() => console.log(`using arrow fn`), 2000);
```
