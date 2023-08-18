# ECMASCRIPT
ECMA Script, often abbreviated as ES, is the standardized scripting language specification developed by Ecma International. It's the foundation for modern JavaScript, which is used extensively in web development for creating dynamic and interactive user interfaces. ES defines the rules, syntax, and features that JavaScript engines should adhere to.

#### ECMAScript 2015 (ES6)
This was a significant update that brought a wide range of new features, including **arrow functions**, **template literals**, **classes**, **modules**, and the **let and const variable declarations**.

## VARIABLE DECLARATIONS

![image](https://github.com/JashandeepSidhu712/MERN-Stack/assets/117754690/e26ab822-e888-422d-a519-9323406023cd)

### var

```
var global = 10; //global variable
function variables()
{
    var sum = 0; //function-scoped
    var i;
    
    for(i=0;i<3;i++)
    {
        sum+=i;
        var index = i; //although it lies inside a loop, but it is accessible in the whole function
    }

    console.log("sum="+sum+" global="+global+" index="+index); //sum = 3 globla=10 index=2
}
variables();
```

### let

```
let global = 10;
function variablesLet()
{
    let sum = 0;
    
    for(i=0;i<3;i++)
    {
        sum+=i;
        let index = i; //accessible only within this loop
    }

    console.log("sum="+sum+" global="+global+" index="+index); //error - index not declared
}
variablesLet();
```

### const
const is a keyword in JavaScript that is used to declare a variable with a constant value. Once a variable is declared with const, its value cannot be changed or reassigned throughout the rest of the code. In other words, const creates a variable that is read-only.

Variables declared with const are block-scoped. This means they are only accessible within the block of code they are declared in.

You cannot declare a const variable without assigning it a value.

```
const a = 10;
a = 20;
console.log(a);
```

## Functions as object
In JavaScript, functions are first-class objects, which means they can be treated like any other object. They have properties and methods just like regular objects.

```
function myFunction() //myFunction is a object
{ 
    // Function body
}
myFunction(); // Using the function name to call the function
```

```
const product=function(p,q)
{
    ans = p*q;
    console.log(ans);
}
product(1,2); //2
```

```
const product=function(p,q)
{
    product.ans = p*q;
    console.log(product.ans);
}
product(1,2); //2
```
