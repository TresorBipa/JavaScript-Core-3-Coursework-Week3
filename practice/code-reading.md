# Code reading
## Question 1
Take a look at the following code:
```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
Functions have their own scope. both variables may have the same name, but they are different variables.
## Question 2

Take a look at the following code:
```
let x = 10
function f1()
{
    console.log(x)
    let y = 20
}
console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
The output of this code will be undefined. x is a global variable and can be used in the function, but y does not exist outside  the function f1(). Therefore, logging it to the console outside the function will result in undefined.

## Question 3

Take a look at the following code:
```
const x = 9;
function f1(val) {
  val = val + 1;
  return val;
}
f1(x);
console.log(x);
const y = { x: 9 };
function f2(val) {
  val.x = val.x + 1;
  return val;
}
f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
Line 54 returns 9 because  primitive data types are passed by value, changes made to the variable in the function don’t affect the initial variable. 
Line 64 return {x:10} because any changes made to an object will be visible to you after the function is done executing.