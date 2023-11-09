##  Turning Strings to URLs

URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.

You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.

Example
Input: "Jasmine Ann Jones"

Output: "Jasmine%20Ann%20Jones"


## Solution 1 with Recursion

const urlConverter = (string) => {
if (string.split(" ").length === 1){
    return string;
  } else {
    const indexNum = string.indexOf(" ");
    string[indexNum] = "
  }
}