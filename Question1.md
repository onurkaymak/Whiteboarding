##  Turning Strings to URLs

URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.

You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.

Example
Input: "Jasmine Ann Jones"

Output: "Jasmine%20Ann%20Jones"


## Solution 1 with Recursion

const urlConverter = (string, index = 0) => {
if (index === string.length){  ///  This means that the function has checked the entire string, and it returns an empty string to end the recursion.
    return ""; 
  } 
  
  if (string[index] === " ") {
    return "%20" + urlConverter(string, index + 1);
  } else {
    return string[index] + urlConverter(string, index + 1);
  }
}