# JAVASCRIPT TIMERS

setInterval and setTimeout are two built-in functions in JavaScript that allow you to schedule the execution of code after a specified amount of time. They are commonly used to create timers, animations, and perform periodic tasks.

## setInterval Function
The setInterval function is used to repeatedly execute a function or a code snippet at a specified interval.

```
const intervalId = setInterval(function() {
    console.log("This will be logged every 2000 milliseconds (2 seconds)");
}, 2000);
```
In this example, the provided function will be executed every 2000 milliseconds (2 seconds) until you explicitly stop it using the clearInterval function.

## setTimeout Function
The setTimeout function is used to execute a function or a code snippet after a specified delay in milliseconds.

```
const timeoutId = setTimeout(function() {
    console.log("This will be logged after 1000 milliseconds (1 second)");
}, 1000);
```

In this example, the function provided as the first argument to setTimeout will be executed after a delay of 1000 milliseconds (1 second). The function returns a timeout ID that you can use to cancel the execution using the clearTimeout function

## Clearing Timers
Both setTimeout and setInterval return a numeric ID that represents the timer. This ID can be used to clear or cancel the timer using the clearTimeout and clearInterval functions respectively.

```
// Clearing a timeout
clearTimeout(timeoutId);

// Clearing an interval
clearInterval(intervalId);
```

### EXAMPLE

```
const fxn=()=>
{
    console.log("me");
}

const ref = setInterval(fxn,1000);

setTimeout(()=>{
    clearInterval(ref);
},10000);
```

## CLOCK

```
const clock=(text)=>
{
    let date = new Date();

    let time = date.getHours()+":"+date.getMinutes()+":"+date.getSeconds();

    console.log(text+" "+time);
}

const ref2 = setInterval(clock, 10000, "Time");

setTimeout(()=>{
    clearInterval(ref2);
},1000000);
```
