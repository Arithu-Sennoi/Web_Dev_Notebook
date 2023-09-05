```js
// useful string properties & methods 
let userName = "Bro Code"; let phoneNumber = "123-456-7890"; console.log(userName.length); 
console.log(userName.charAt(0)); 
console.log(userName.indexOf("o")); 
console.log(userName.lastIndexOf("o")); 
userName = userName.trim(); 
userName = userName.toUpperCase(); 
userName = userName.toLowerCase(); 
phoneNumber = phoneNumber.replaceAll("-", "");
console.log(phoneNumber);
```

`indexOf()` gives index of first occurance of given character in the string. 

`trim()` would remove all unnecessary spaces at the start and end of the string.

`userName.length` will give length of the string stored in variable userName. Notice that it doesn't have curly braces at the end of .length keyword.

