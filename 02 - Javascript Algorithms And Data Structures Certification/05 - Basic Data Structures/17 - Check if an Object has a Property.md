# Check if an Object has a Property

Now we can add, modify, and remove keys from objects. But what if we just wanted to know if an object has a specific property? JavaScript provides us with two different ways to do this. One uses the `hasOwnProperty()` method and the other uses the `in` keyword. If we have an object `users` with a property of `Alan`, we could check for its presence in either of the following ways:

```js
users.hasOwnProperty('Alan');
'Alan' in users;
// both return true
```

---

## challenge

We've created an object, `users`, with some users in it and a function `isEveryoneHere`, which we pass the `users` object to as an argument. Finish writing this function so that it returns `true` only if the `users` object contains all four names, `Alan`, `Jeff`, `Sarah`, and `Ryan`, as keys, and `false` otherwise.

---

## Tips

- The `users` object only contains the keys `Alan`, `Jeff`, `Sarah`, and `Ryan`

- The function `isEveryoneHere` returns `true` if `Alan`, `Jeff`, `Sarah`, and `Ryan` are properties on the users object

- The function `isEveryoneHere` returns `false` if `Alan`, `Jeff`, `Sarah`, and `Ryan` are not properties on the `users` object

---

## Solution

```js
let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(obj) {
  // change code below this line
return 'Alan' in users && 'Jeff' in users && 'Sarah' in users && 'Ryan' in users;
  // change code above this line
}

console.log(isEveryoneHere(users));
```