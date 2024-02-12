-  [[Hooks]]
-  [[Bundle]]
-  [[react-query]]
-  [[rtk query]]
-  [[issues on calling api request using fetch inside useEffect]]
	1. strict mode logs twice
[[crucial]]

## Frequently asked
- A closure is a fundamental concept in JavaScript, and it occurs when a function is defined inside another function and has access to the outer function's variables. A closure "closes over" the variables in its lexical scope, allowing it to retain access to those variables even when the outer function has finished executing.
```js
function outerFunction() {
  let outerVariable = 'I am from the outer function';

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

const closureExample = outerFunction();
closureExample(); // Outputs: "I am from the outer function"

```


