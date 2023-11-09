## Question #2: Array Deduping

Write an algorithm that removes duplicates from an array. Do not use a function like filter() to solve this. Once you have solved the problem, demonstrate how it can be solved with filter(). Solve the problem with and without recursion.

Example
Input: [7, 9, "hi", 12, "hi", 7, 53]

Output: [7, 9, "hi", 12, 53]

const deduper = (array) => {
  let newArr = [];

  for(let i = 0; i <= array.length; i++){
    if (array[i] !== array[i + 1]) {
      newArr.push(array[i]);
    } else {
      return
    }
    return newArr;
  }
}

  array.map((element, index) => if (index) {

  })