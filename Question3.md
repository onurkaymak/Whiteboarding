## Question #3: Compressing Strings

Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.

Example
Input: "aaabccdddda"

Output: "3ab2c4da"

// It only works for the first element
## Solution 1 w/o Recursion (Unsolved) 

const stringCompressor = (string) => {
  let compArr = [];
  let count = 0;
  let currChar = string[0];

  for (let i = 0; i < string.length; i++) {
    if (string[i] === currChar) {
      count ++;
    } else {
      if (count > 1){
        compArr.push(count + currChar);
        currChar = string[i];
        count = 1;  
      } 
        compArr.push(currChar);  
    }
  }
  return compArr;
};