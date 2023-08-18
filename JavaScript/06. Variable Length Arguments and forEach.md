# VARIABLE LENGTH ARGUMENTS
Variable-length arguments, also known as **variadic arguments or varargs**, allow a function to **accept an arbitrary number of arguments**, regardless of how many arguments were defined in the function's parameter list.


## Using the arguments Object
In JavaScript, functions have access to a **special object called the arguments object**. It **holds all the arguments passed to the function**, **even if they are not explicitly defined in the function's parameter list**.

However, using the arguments object has some limitations, such as not being an actual array (it's an array-like object) and not supporting modern array methods.

## The ... syntax, known as the "spread/rest" operator

### Rest Parameter
The rest parameter is used in function declarations to collect multiple arguments into a single array parameter. This is particularly useful when dealing with functions that accept a variable number of arguments.

They allow you to capture all remaining arguments into a single array parameter.

#### using loops

```
let args = (... array)=>
{
    for(i=0;i<array.length;i++)
    console.log(array[i]);
}
args(1,2,3,4,5,6,7,8,9);
```

#### using forEach
The forEach method is a built-in JavaScript function that is used to iterate over the elements of an array and execute a provided function once for each element. 

It's a convenient way to perform an operation on each element of an array without the need for writing a traditional for loop.

SYNTAX
```
array.forEach(function(currentValue, index, array) {
    // Code to be executed for each element
});
```

**currentValue**: The current element being processed in the array. <br>
**index**: The index of the current element in the array. <br>
**array**: The array on which forEach is being called. <br>

```
let args2 = (... array)=>
{

    console.log("using foreach");
    array.forEach(function(value, index){
        console.log(value+" "+index);
    })
}
args2(1,2,3,4,5,6,7,8,9);
```

## EXTRACTING ONLY EVEN VALUES AND STORING IN NEW ARRAY

```
const even = []; //This code snippet declares a constant array variable named even and initializes it with an empty array.
let evenArgs = (... array)=>
{

    array.forEach(function(value, index){
        if(value%2==0)
        {
            // console.log(value+" "+index);
            even.push(value); //The code even.push(1); adds the value 1 to the end of the array stored in the even variable. 
        }
        
    })
}
console.time();
evenArgs(1,2,3,4,5,6,7,8,9);
console.log("EVEN ARRAY VALUES");
console.log(even); //OUTPUT [ 2, 4, 6, 8 ]
console.log(even.pop()); // OUTPUT 8
console.log(even); //OUTPUT [ 2, 4, 6]
console.timeEnd();

```

## shift() and unshift()
They are used to manipulate the contents of an array by adding or removing elements from the beginning of the array.

### shift() Method
The shift() method removes the first element from the array and returns it. 

This operation also shifts the remaining elements one position to the left, effectively reducing the length of the array by one.

```
const numbers = [1, 2, 3, 4, 5];
const removedNumber = numbers.shift();

console.log(removedNumber); // Output: 1 (removed element)
console.log(numbers); // Output: [2, 3, 4, 5]
```

###  unshift() Method
The unshift() method adds one or more elements to the beginning of the array and returns the new length of the array.

```
const numbers = [2, 3, 4, 5];
const newLength = numbers.unshift(1);

console.log(newLength); // Output: 5 (new length of the array)
console.log(numbers); // Output: [1, 2, 3, 4, 5]
```
