# core-code-from-scratch-25-01-

## ---Easy mathematical callback---

* [Test](https://www.codewars.com/kata/54b7c8d2cd7f51a839000ebf/train/javascript)

Solution / /

``` javascript
function processArray(arr, callback) {
    let newArr = [];
  for(let i=0; i<arr.length;i++){
    newArr.push(callback(arr[i]));
  }
  return newArr;
}
```
---

## ---Moving Zeros to the End---

* [Test](https://www.codewars.com/kata/52597aa56021e91c93000cb0/train/javascript)

Solution 1 / /

``` javascript 
function moveZeros(arr) {
  let zeros = arr.filter( x => x === 0);
  let notZero = [];
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] !== 0) {
      notZero.push(arr[i]);
    }
  }
  const result = notZero.concat(zeros);
  return result;
}
```

Solution 2 / /

``` javascript 
function moveZeros(arr) {
  let filter = arr.filter(num => num !== 0);
  let zeros = arr.filter(num => num === 0);
  let result = filter.concat(zeros);
  return result
}
```
---

## ---Valid Parentheses

* [Test](https://www.codewars.com/kata/52774a314c2333f0a7000688/train/javascript)

Solution / /

``` javascript 
function validParentheses(parens) { 
  let counter = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === ')') counter--;
    if (parens[i] === '(') counter++;
    if (counter < 0) return false;
    }
  return counter == 0;
}
```

---
## ---Knowledge Base---
* [Callbacks](https://developer.mozilla.org/es/docs/Glossary/Callback_function)
* [Array Filter method](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
* [Array Reduce method](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
