## Question #4: Checking for Uniqueness

Write an algorithm that determines whether all the elements in a string are unique. You may not convert the string into an array or use array methods to solve this problem. The algorithm should return a boolean.

Example
Input: "hello"

Output: false

Input: "copyright"

Output: true

## Solution 1 with Recursion 


const isUnique = (string, index = 0) => {
  let indexLetter = string[index]
  let slicedWord = string.slice(index + 1);
  let bool;

  if (slicedWord.includes(indexLetter)){
     bool = false
  } else {
    isUnique(string, index + 1);
  }
  return bool;
}

## Solution 2 

const isUnique = (string) => {
  let charCount = {};

  for (let i = 0; i < string.length; i++) {
    let char = string[i];

    if (charCount[char]) {
      return false;
    } else {
      charCount[char] = 1;
    }
  }
  return true;
};


