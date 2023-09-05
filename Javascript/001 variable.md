3 ways to create a variable: var, let, const. 

const is for later. 

Between ver and let, let is more preferable, because of variable scope. We will learn it later. 

```javascript
let firstname = "bro";
let age;
let student = true; 

console.log(firstname);//output: bro
console.log("hello", firstname);//output: hello bro

age=21;
console.log(age);//this would print: 21
age++
console.log(age);//this would print: 22
console.log("hello, you are ", age, " years old!")
//output:hello, you are 22 years old!
console.log("enrolled:", student);//output: enrolled: true


```

Note: In javascript, if you add a number to a string, it would convert that number into a string, and concantenate both strings. 


when you create a variable using let, and did not assign it, it will be a string. 
Then, if you collect input from user, then it will store that input as a string. 

```javascript
let age=window.prompt("what is your age?");

age+=1;

console.log(age);//output:211
```
here, the age is a string, and when we add 1 to it, it would concantenate it. 

to avoid this issue, we convert age into an interger. 

```javascript
let age = window.prompt("what is your age?");
age = Number(age);
age += 1;

console.log(age);
```

