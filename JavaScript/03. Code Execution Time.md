# JAVASCRIPT PERFORMANCE PROFILING WITH CONSOLE.TIME() AND CONSOLE.TIMEEND()
In JavaScript, console.time() and console.timeEnd() are **methods provided by the console object** that allow you to **measure the time taken by a portion of your code**. 

These methods are commonly used for performance profiling and benchmarking to understand how long a specific operation or piece of code takes to execute.

## console.time(label)
This method starts a timer with a specified label. 

The label is a string that you provide to identify the timer. You can have multiple timers running simultaneously with different labels.


## console.timeEnd(label)
This method stops the timer with the specified label and logs the time elapsed since console.time() was called with the same label. 

The time is displayed in milliseconds.

### SYNTAX

```
console.time("myTimer");
// Code you want to measure
// Code you want to measure
console.timeEnd("myTimer");
```

### EXAMPLE

```
console.time("myTimer");

for (let i = 0; i < 1000000; i++) {
    // Some operation to be measured
}

console.timeEnd("myTimer");  //OUTPUT - myTimer: 13.121ms

```
