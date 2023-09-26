At their most basic, objects are just collections of key-value pairs. In other words, they are pieces of data (values) mapped to unique identifiers called properties (keys). Take a look at an example:
```js
const tekkenCharacter = {
  player: 'Hwoarang',
  fightingStyle: 'Tae Kwon Doe',
  human: true
};
```

The above code defines a Tekken video game character object called `tekkenCharacter`. It has three properties, each of which map to a specific value. If you want to add an additional property, such as "origin", it can be done by assigning `origin` to the object:
```js
tekkenCharacter.origin = 'South Korea';
```

This uses dot notation. If you were to observe the `tekkenCharacter` object, it will now include the `origin` property. Hwoarang also had distinct orange hair. You can add this property with bracket notation by doing:
```js
tekkenCharacter['hair color'] = 'dyed orange';
```

Bracket notation is required if your property has a space in it or if you want to use a variable to name the property. In the above case, the property is enclosed in quotes to denote it as a string and will be added exactly as shown. Without quotes, it will be evaluated as a variable and the name of the property will be whatever value the variable is. Here's an example with a variable:

```js
const eyes = 'eye color';

tekkenCharacter[eyes] = 'brown';
```

After adding all the examples, the object will look like this:
```js
{
  player: 'Hwoarang',
  fightingStyle: 'Tae Kwon Doe',
  human: true,
  origin: 'South Korea',
  hair color: 'dyed orange',
  eye color: 'brown'
};
```

Just use bracket notiation. So you won't be confused. Since objects are like objects in C++, but also like hashmap in C++. But I will use bracket notation since I have used hashmap more often, and I got used to it. 
But do remember to put quotes for strings in bracket notation. You do not need them for dot notation, but you do need them for bracket. 

If you try to access a key-value pair in object, that is not present in that object, you will get undefined as the value for that key. 
### nested objects
```js
let userActivity = {
	id: 23894201352,
	date: 'January 1, 2017',
	data: {
		totalUsers: 51,
		online: 42
	}
};
userActivity['data']['online'] = 42;

console.log(userActivity);
```
Above uses bracket notation to update the value of online, in `data` object which is inside the `userActivity` object. 

### delete keyword in objects
You can delete a key-value pair inside an object with delete keyword. See the example below:
```js
let foods = {
apples: 25,
oranges: 32,
plums: 28,
bananas: 13,
grapes: 35,
strawberries: 27
}

delete foods.apples;
console.log(foods);
/*
Output:
	oranges: 32,
	plums: 28,
	bananas: 13,
	grapes: 35,
	strawberries: 27
*/
```
That is how you use delete keyword to delete key-value pairs in objects. 

### Check if an object has a property
we can add, modify, and remove keys from objects. But what if we just wanted to know if an object has a specific property? JavaScript provides us with two different ways to do this. One uses the `hasOwnProperty()` method and the other uses the `in` keyword. If we have an object `users` with a property of `Alan`, we could check for its presence in either of the following ways:

```js
users.hasOwnProperty('Alan');
'Alan' in users;
```

Both of these would return `true`.
### Iterate through the keys of an object
Sometimes you need to iterate through all the keys within an object. You can use a for...in loop to do this. The for...in loop looks like:

```javascript
const refrigerator = {
  'milk': 1,
  'eggs': 12,
};

for (const food in refrigerator) {
  console.log(food, refrigerator[food]);
}
```

This code logs `milk 1` and `eggs 12`, with each key-value pair on its own line.

We defined the variable `food` in the loop head and this variable was set to each of the object's keys on each iteration, resulting in each food's name being printed to the console.

**NOTE:** Objects do not maintain an ordering to stored keys like arrays do; thus a key's position on an object, or the relative order in which it appears, is irrelevant when referencing or accessing that key.

### Generate an Array of All Object Keys with Object.keys()
We can also generate an array which contains all the keys stored in an object with the `Object.keys()` method. This method takes an object as the argument and returns an array of strings representing each property in the object. Again, there will be no specific order to the entries in the array.
```js
let users = {
Alan: {
age: 27,
online: false
},
Jeff: {
age: 32,
online: true
},
Sarah: {
age: 48,
online: false
},
Ryan: {
age: 19,
online: true
}
};
  
function getArrayOfUsers(obj) {
return Object.keys(obj)
}

console.log(getArrayOfUsers(users));
//output:[ 'Alan', 'Jeff', 'Sarah', 'Ryan' ]
```