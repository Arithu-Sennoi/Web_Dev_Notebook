#### from freecodecamp.org
ES6 provides a new syntax to create objects, using the class keyword.

In ES5, an object can be created by defining a `constructor` function and using the `new` keyword to instantiate the object.

In ES6, a `class` declaration has a `constructor` method that is invoked with the `new` keyword. If the `constructor` method is not explicitly defined, then it is implicitly defined with no arguments.

```js
// Explicit constructor
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
  takeOff() {
    console.log("To " + this.targetPlanet + "!");
  }
}

// Implicit constructor 
class Rocket {
  launch() {
    console.log("To the moon!");
  }
}

const zeus = new SpaceShuttle('Jupiter');
// prints To Jupiter! in console
zeus.takeOff();

const atlas = new Rocket();
// prints To the moon! in console
atlas.launch();
```

It should be noted that the `class` keyword declares a new function, to which a constructor is added. This constructor is invoked when `new` is called to create a new object.

**Note:** UpperCamelCase should be used by convention for ES6 class names, as in `SpaceShuttle` used above.

The `constructor` method is a special method for creating and initializing an object created with a class. You will learn more about it in the Object Oriented Programming section of the JavaScript Algorithms And Data Structures Certification.


The constructor method takes parameters. It creates new object properties, and assigns that parameters to the that instance of that class. 
```js
class Vegetable {
	constructor(veggie){
		this.name = veggie;
	}
}
const carrot = new Vegetable('carrot');
console.log(carrot.name); // Should display 'carrot'
```
Here, there is a class called Vegetable. Inside it, there is an argument. Inside the body of the constructor, we set value of name equal to the given argument, using this keyword. The name property doesn't exist, and it being created here. It should be declared again, since it is alreadly being declared by js. 
