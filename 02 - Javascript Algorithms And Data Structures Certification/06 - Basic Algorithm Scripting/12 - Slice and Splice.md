# Slice and Splice

You are given two arrays and an index.

Use the array methods `slice` and `splice` to copy each element of the first array into the second array, in order.

Begin inserting elements at index `n` of the second array.

Return the resulting array. The input arrays should remain the same after the function runs.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

---

## Tips

- `frankenSplice([1, 2, 3], [4, 5], 1)` should return `[4, 1, 2, 3, 5]`.

- `frankenSplice([1, 2], ["a", "b"], 1)` should return `["a", 1, 2, "b"]`.

- `frankenSplice(["claw", "tentacle"], ["head", "shoulders", "knees", "toes"], 2)` should return `["head", "shoulders", "claw", "tentacle", "knees", "toes"]`.

- All elements from the first array should be added to the second array in their original order.

- The first array should remain the same after the function runs.

- The second array should remain the same after the function runs.

---

## Solution

```js
function frankenSplice(arr1, arr2, n) {
  // It's alive. It's alive!
  let x = [...arr1];
  let y = [...arr2];
  for (let i in x){
    y.splice(n,0,x[i]);
    n++;
  }
  return y;
}

frankenSplice([1, 2, 3], [4, 5, 6], 1);
```