```javascript
/**
 * Find the element that appears once
 */

// let arr = [12, 1, 12, 3, 12, 1, 1, 2, 3, 3];
// let arr = [10, 20, 10, 30, 10, 30, 30];
let arr = [5, 5, 5, 8];
let obj = {};
let value = [];
for (var i = 0; i < arr.length; i++) {
  obj[arr[i]] = obj[arr[i]] === undefined ? 1 : obj[arr[i]] + 1;
}

let keys = Object.keys(obj);

const res = keys.reduce((acc, curr) => {
  if (obj[curr] === 1) {
    acc = curr;
  }
  return Number(acc);
}, 0);
console.log(res); // 8
```
