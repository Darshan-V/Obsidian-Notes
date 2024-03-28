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

### ___[jsv8engine and node](https://cabulous.medium.com/how-v8-javascript-engine-works-5393832d80a7)___


- [ ] What is a single page application
- [ ] To build a static web-page, with just header, bg and a p tag, which option is better and why?, using vanilla js or using react , angular, vue or any library or framework.
- [ ] why react
- [ ] what is the difference in building frontend using vanilla js and react
- [ ] what is virtual dom
- [ ] what are the disadvantages or advantages of not having virtual dom
- [ ] What is react suspense
- [ ] Explain how authentication flow / how to handle authentication
- [ ] 