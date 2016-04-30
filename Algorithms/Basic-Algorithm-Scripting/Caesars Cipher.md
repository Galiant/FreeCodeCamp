# Caesars Cipher

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

### Here are some helpful links:

+ [String.charCodeAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)
+ [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)

### Task

+ rot13("SERR PBQR PNZC") should decode to "FREE CODE CAMP"
+ rot13("SERR CVMMN!") should decode to "FREE PIZZA!"
+ rot13("SERR YBIR?") should decode to "FREE LOVE?"
+ rot13("GUR DHVPX OEBJA QBT WHZCRQ BIRE GUR YNML SBK.") should decode to "THE QUICK BROWN DOG JUMPED OVER THE LAZY FOX."

### Solution

```javascript
function rot13(str) { // LBH QVQ VG!
  var decoded="";
    for (var i in str) {
        if (str.charCodeAt(i) < 65 || str.charCodeAt(i) > 91) { // check if char is outside A-Z range
            decoded += str[i];
            continue;
        }
        // chars A-M will loop back over Z, so you need to add 13(26-13)
        if (str.charCodeAt(i) < 78) {
            decoded += String.fromCharCode(str.charCodeAt(i) + 13);
        }
        // all remaining chars - N-Z
        else {
            decoded += String.fromCharCode(str.charCodeAt(i) - 13);
        }
    }
    return decoded;
}
// Change the inputs below to test
rot13("SERR PBQR PNZC");
```
