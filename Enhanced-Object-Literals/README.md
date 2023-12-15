## What is it?

Enhanced object literals, introduced in ES6, are a set of enhancements to the syntax for defining objects in JavaScript. These enhancements make it more convenient and concise to define object properties and methods.

## When Name and Value is Same

If name and value pairs are the same we can directly use the name instead.

Example-1 (Creating new variables from values of an object.)

```js
const object1 = {
  name: "Tushar",
  age: 16,
};

const { name, age } = object1;
console.log(name); //'Tushar'
console.log(age); //16
```

Example-2 (Creating an object using a function)

Before - Old Way

```js
const person = (name, age, course) => {
  return {
    name: name,
    age: age,
    course: course,
  };
};

console.log(person("Tushar", 16, "MERN-Stack"));
```

After - New Way

```JS
const person = (name, age, course) => {
return {
        name,
        age,
        course,
    };
};

console.log(person("Tushar", 16, "MERN-Stack"));
```

## Object Methods - Shorthand property

We can use shortcuts when declaring methods.

Before - Old way

```js
const object1 = {
  name: "Tushar",
  age: 16,
  intro: function () {
    return `Name is ${this.name} and age is ${this.age}`;
  },
};
console.log(object1.intro());
//Name is Tushar and age is 16
```

After - New Way

```js
const object1 = {
  name: "Tushar",
  age: 16,
  intro() {
    return `Name is ${this.name} and age is ${this.age}`;
  },
};
console.log(object1.intro());
//Name is Tushar and age is 16
```
