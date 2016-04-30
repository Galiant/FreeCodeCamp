# Confirm the Ending

Check if a string (first argument, str) ends with the given target string (second argument, target).

Remember to use Read-Search-Ask if you get stuck. Write your own code.

### Here are some helpful links:

+ [String.substr()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)

### Task

+ confirmEnding("Bastian", "n") should return true.
+ confirmEnding("Connor", "n") should return false.
+ confirmEnding("Walking on water and developing software from a specification are easy if both are frozen", "specification") should return false.
+ confirmEnding("He has to give me a new name", "name") should return true.
+ confirmEnding("He has to give me a new name", "me") should return true.
+ confirmEnding("He has to give me a new name", "na") should return false.
+ confirmEnding("If you want to save our world, you must hurry. We dont know how much longer we can withstand the nothing", "mountain") should return false.

### Solution

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  var sub = str.substring(str.length - target.length);
  if (sub === target) {
    return true;
  } else {
    return false;
  }
}

confirmEnding("He has to give me a new name", "name");
```
