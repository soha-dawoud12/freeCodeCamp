# DNA Pairing

The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

[Base pairs](http://en.wikipedia.org/wiki/Base_pair) are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

---

## Tips

- `pairElement("ATCGA")` should return `[["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]]`.

- `pairElement("TTGAG")` should return `[["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]]`.

- `pairElement("CTCTA")` should return `[["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]]`.

---

## Solution

```js
function pairElement(str) {
  let newArr = [];
  let finalArr = [];
  for (let i in str){
    newArr.push(str[i]);
    switch(str[i]){
      case "G":
        newArr.push("C");
        break;
      case "C":
        newArr.push("G");
        break;
      case "A":
        newArr.push("T");
        break;
      case "T":
        newArr.push("A");
        break;
    }    
    finalArr.push(newArr);
    newArr = [];
  }
  return finalArr;
}

//pairElement("GCG");
//pairElement("ATCGA");// should return [["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]].
pairElement("TTGAG");// should return [["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]].
//pairElement("CTCTA");// should return [["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]].
```