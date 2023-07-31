# JavaScript Quiz

## Multiple Choice Questions (MCQs)

1. What will the following code output: `console.log(typeof null);`
    A. "null"
    B. "NaN"
    C. "undefined"
    **D. "object"**

2. What will the following code output: `console.log(0.1 + 0.2 === 0.3);`
    A. true
    **B. false**
    C. NaN
    D. Error

3. Which method is used to remove the last element from an array and returns that element?
    A. push()
    B. shift()
    **C. pop()**
    D. unshift()

4. How to create a date object for the current date and time in JavaScript?
    **A. new Date()**
    B. Date.now()
    C. Date()
    D. Date.get()

5. What is the output of `"10" + 2` in JavaScript?
    A. 12
    **B. "102"**
    C. "12"
    D. Error

## Code Writing Questions

1. Write a JavaScript function to clone an array.
function cloneArray(arr) {
  return [...arr];
}

2. Write a JavaScript function that takes a string and returns it in reverse order.
function reverseString(str) {
  let reversedString = '';
  for (let i = str.length - 1; i >= 0; i--) {
    reversedString += str.charAt(i);
  }
  return reversedString;
}

3. Write a JavaScript function to get the value of π (pi) up to n number of decimal places.
// Javascript program to calculate the
    // value of pi up to n decimal places
     
    // Function that prints the
    // value of pi upto N
    // decimal places
    function printValueOfPi(N)
    {
      
        // Find value of pi upto
        // using acos() function
        let pi = 2 * Math.acos(0.0);
      
        // Print value of pi upto
        // N decimal places
        document.write(pi.toFixed(4));
    }
     
    let N = 4;
      
    // Function that prints
    // the value of pi
    printValueOfPi(N);


4. Write a JavaScript function to merge two objects.
function mergeObjects(obj1, obj2) {
  return Object.assign({}, obj1, obj2);
}


5. Write a JavaScript function to create a deep copy of an object.
function deepCopy(obj) {
  if (obj === null || typeof obj !== 'object') {
    return obj;
  }

  let copy;
  if (obj instanceof Array) {
    copy = [];
    for (let i = 0; i < obj.length; i++) {
      copy[i] = deepCopy(obj[i]);
    }
  } else {
    copy = {};
    for (const key in obj) {
      if (Object.prototype.hasOwnProperty.call(obj, key)) {
        copy[key] = deepCopy(obj[key]);
      }
    }
  }

  return copy;
}

