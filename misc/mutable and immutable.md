Data types that can be changed later after declaring are called mutable data type. 
Immutable data type is something that cannot be changed once declared and assigned. 

### Const keyword.
If you declare something with const keyword, you cannot assign that variable some other value. 
But you can modify that data type. Let me explain.

If you delcare a variable holding integer value using let keyword, you obviously can assign that variable a new value. But if you declare it with a `const` keyword, you cannot assign it a new value. 
assigning a value to a variable is not same as modifying the value within that variable. 
Consider an array. If you declare it like this: `const myArray = [5, 6, 7];` then you cannot assign it a new array. But you can modify the existing array without `myArray` variable. You can change it's values, etc. 
You cannot do that with an integer variable, becuase regardless of what operation you perform, you are basically re assigning that variable. With an array, you could modify the value inside the variable without re assigning that array. 
Hence, arrays declared with `const` keyword are still mutable. 