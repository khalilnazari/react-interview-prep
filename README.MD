# React-JS Interview Preparation 
## Coding Questions 
### 1. JavaScript Coding Questions 

1. Write a function that counts all vowels in a sentence
```
let sentence = "I am a programmer and I love JavaScript."; 
const vowelsArray = ['a', 'e', 'i', 'o', 'u']
let vowelsCount = 0; 

// 1. Using .match()
vowelsCount = sentence.match(/[aeuio]/gi) ? sentence.match(/[aeuio]/gi).length : 0;
```
```
// 2. Using .test()
for (let char of sentence) {
    if (/[aeiou]/gi.test(char.toLowerCase())) {
        vowelsCount++
    }
}
```
```
// 3. Using .includes()
for (let char of sentence) {
    if (vowels.includes(char.toLowerCase())) {
        vowelsCount++
    }
}

console.log(vowelsCount) // 13
```

2. Reverse a string in JavaScript 
```
// 1. Using built-in methods 
let reversedSentence = sentece.split("").reverse().join("")
```
```
// 2. Using .forEach()
reversedSentence = '';
sentence.splite("").forEach(char => {
  reversedSentence = char + reversedSentence; 
})
```
```
// 3. Using .reduce(); 
reversedSentence = sentence.split("").reduce((prev, curr) => curr + prev, '')

console.log(reversedSentenct) 
```

3. Write a function that returns if string a palindrome
```
let simpleString = "eye"

// 1. Using .reverse() and .join()
let palindromeString = simpleStr.split('').reverse().join('') === str; // true 
```
```
// 2. Using .every(); 
let simpleString = "javascript"
simpleString.split('').every((char, index) => char === str[simpleString.length - index - 1]); // false 
```

4. Write a function that will remove duplicate in an array 
```
let arr = [2, 3, 4, 55, 2, 3]
// 1. Using ES6 Set()
function removeDuplicates(array) {
  return [...new Set(array)]
}
```
```
// 2. Using Object 
function removeDuplicates(array) {
  const map = {}

  for (const char of array) {
    if (map[char]) {
      map[char]++
    } else {
       map[char] = 1
    }
  }

  return Object.keys(map)
}
```

5. Javascript function to return min and max values in an array 
```
// 1. Using Math methods 
function getMinMax(arr) {
  return {
    min: Math.min( ...arr ),
    max: Math.max( ...arr )
  }
}
```
```
// 2. Using .sort()
function getMinMax(arr) {
  const sortedArray = arr.sort((a, b) => a - b)

  return {
    min: sortedArray[0],
    max: sortedArray[sortedArray.length - 1]
  }
}
```

6. Using Javascript print from 1 to 100. Print 'fizz' for multiples for 3, 'buzz' for multiples of 5, and 'fizzbuzz' for multiples of 3 and 5. (one-liner)
```
for(let i=1; i<=100; i++) {
  const text = i%3===0 ? "fizz" ? i%5===0 "fuzz" ? (i%3===0 && i%5===0) ? "fizzbuzz" : i
}
```

7. Using JS capitalize each word of a sentence. 
```
// 1. Using .split() and .map()
let capitalizedSentence = sentence.split(" ").map(wrod => word[0].toUpperCase() + word.slice(1)).join(' ')
```
```
// 2. Using reduce()
let capitalizedSentence = sentence.split(" ").reduce((prev, curr) => `${prev} ${curr[0].toUpperCase() + curr.slice(1)}`, '')
```

8. Get the most repeated character in a string 
```
let str = "I am a javascript developer"
let normalizeStr = (str) => str.replace(/[^\w]/g, '').toLowerCase()
const getMostRepeatedChar = (str) => {
  const charMap = {}
  let max = 0
  let maxChar = ""

  for (let char of normalizeStr(str)) {
    if (charMap[char]) {
      charMap[char]++
    } else {
      charMap[char] = 1
    }
  }

  for (let char in charMap) {
    if (charMap[char] > max) {
      max = charMap[char]
      maxChar = char
    }
  }

  return maxChar
}

console.log(getMostRepeatedChar(str))

```

9. Check balanced parentheses using JS
```
const isBalancedParentheses = (str) => {
    let count = 0;
    for (let char of str)
    {
        if (char === '(') { count++; }
        else if (char === ')')
        {
            if (count === 0) { return false; }
            count--;
        }
    }
    return count === 0;
}

console.log(isBalancedParentheses("(this is testing)")) // true
console.log(isBalancedParentheses("(this is testing")) // false
```

10. Differences between null and undefined
```
// a is declared but it does not have any value. Therefore, it is undefined. 
let a; 
console.log(a) // undefined

// Here a has a value which a null (null a special value === no value)
a = null; 
console.log(a) // null 

// Here a got a value of 5 (real value)
a = 5; 
console.log(a) // 5
```

11. Whats && operator in JS? 
The && or Logical AND operator finds the first falsy expression in its operands and returns it and if it does not find any falsy expression it returns the last expression. 
```
console.log(false && 1 && []); // false
console.log(" " && true && 5); // 5

// we can use && or AND operator in conditinal 
let test = false; 
if(test) {
    console.log("it will not be logged")
}

test && "it will not be logged again."

test = true; 
test && "it will not be logged here."

```

12.  What does the || operator do?
The || or Logical OR operator finds the first truthy expression in its operands and returns it.

console.log(null || 1 || undefined); // 1
console.log(name || "Mark") // Mark 
