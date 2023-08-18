# ARROW FUNCTION
Arrow functions, introduced in ECMAScript 6 (ES6), provide a more concise syntax for creating functions in JavaScript. They are often used for shorter, inline functions and have some unique characteristics compared to traditional function expressions.


### Traditional function

```
const sum=function(aa,bb)
{
    ans = aa+bb;
    console.log(ans);
}
sum(1,2); //3
```

### Arrow function

#### multiple lines

```
const sum2=(aa,bb)=>
{
    ans = aa+bb;
    console.log(ans);
}
sum2(1,2); //3
```

```
const multi=(a,b)=>
{
    sum = a+b;
    return sum;
}
console.log(multi(1,3));
```

#### single line
Arrow functions have an implicit return when the function body is a single expression. You don't need to explicitly use the return keyword.

```
const single=(a,b)=> a+b;
console.log(single(1,2));
```

#### single parameter 

```
const sqr=s=> s*s;
console.log(sqr(10));
```

## IIFE
An IIFE (**Immediately Invoked Function Expression**) is a common JavaScript design pattern that **involves creating a function expression and immediately invoking it**.

This pattern is often used to create a **private scope for variables**, **prevent pollution of the global namespace**, and **execute code immediately after it's defined**. When arrow functions are used within IIFEs, they maintain the same behavior but with some considerations due to their characteristics.

#### In traditional

```
(function() {
    // Function body
})();

```

```
(function message()
{
    const message = "Hello from IIFE!";
    console.log(message);
})();
```

#### in arrow function
In an arrow function IIFE (Immediately Invoked Function Expression), you don't need to write the function keyword and provide a function name. Arrow functions provide a concise syntax that allows you to create anonymous functions, making them well-suited for IIFEs.

```
(() => {
    // Function body
})();
```

```
(() =>
{
    const message = "Hello from IIFE!";
    console.log(message);
})();
```
