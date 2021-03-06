# Nesting For Loops

If you have a multi-dimensional array, you can use the same logic as the prior waypoint to loop through both the array and any sub-arrays. Here is an example:

```js
var arr = [
  [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
  for (var j=0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

This outputs each sub-element in `arr` one at a time. Note that for the inner loop, we are checking the `.length` of `` ``, since `arr[i]` is itself an array.

---

## Challenge

Modify function `multiplyAll` so that it multiplies the `product` variable by each number in the sub-arrays of `arr`

---

## Tips

- `multiplyAll([[1],[2],[3]])` should return `6`

- `multiplyAll([[1,2],[3,4],[5,6,7]])` should return `5040`

- `multiplyAll([[5,1],[0.2, 4, 0.5],[3, 9]])` should return `54`

---

## Solution

```js
function multiplyAll(arr) {
  var product = 1;
  // Only change code below this line
  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < arr[i].length; j++) {
      product *= arr[i][j];
    }
  }
  // Only change code above this line
  return product;
}

// Modify values below to test your code
multiplyAll([[1,2],[3,4],[5,6,7]]);
```