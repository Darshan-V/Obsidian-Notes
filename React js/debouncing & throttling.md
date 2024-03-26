## Debouncing

* custom debouncing hook
```javascript
const useDebounce = (func, delay) => {
    let timeout=null

    return (...args) => {
        if(timeout) clearTimeout(timeout)

        timeout=setTimeout(() => {
            func(...args)
        }, delay)
    }
}

export default useDebounce```

- debouncing is used mostly in search or auto-complete functions, where a function or api call is made when the user stops typing.
## Throttling
- throttling is a technique that limits how often a function can be called in an interval
```javascript
function throttle(mainFunction, delay) {
  let timerFlag = null; // Variable to keep track of the timer

  // Returning a throttled version 
  return (...args) => {
    if (timerFlag === null) { // If there is no timer currently running
      mainFunction(...args); // Execute the main function 
      timerFlag = setTimeout(() => { // Set a timer to clear the timerFlag after the specified delay
        timerFlag = null; // Clear the timerFlag to allow the main function to be executed again
      }, delay);
    }
  };
}

```
#### use case
``` javascript

// Define a function that fetches some data from an API
function fetchData() {
  console.log("Fetching data...");
  // Simulate an API call with a random delay
  setTimeout(() => {
    console.log("Data fetched!");
  }, Math.random() * 1000);
}

// Throttle the fetchData function with a delay of 5000 ms
const throttledFetchData = throttle(fetchData, 5000);

// Add an event listener to the window scroll event that calls the throttledFetchData function
window.addEventListener("scroll", throttledFetchData);
```
