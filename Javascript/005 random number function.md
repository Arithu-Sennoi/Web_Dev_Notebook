```js
let x = Math.random(); 
console.log(x);
```
this would give a random decimal number between 0 and 1. 
if you multiply it by 6, it would give a random number between 0 and 6 exculsive. 

if you just want intergers, then round it. 
```js
let x = Math.random()*6;
x = Math.round(x);
console.log(x);
```
this will output a random integer ranging from 0 to 5. 

if we want to make a dice that would generate a random number from 1 to 6, here is the code:
```js
let roll = Math.random() * 6 + 1;
x = Math.round(x);
console.log(x);
```
