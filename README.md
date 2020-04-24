```js
// ******* QUESTION 1 *******
// Write a method or function that takes an array of numbers and returns the average of the numbers in the array.

const averageNum = numArr => {
  let sum = 0; 
  for (let i = 0; i < numArr.length; i++){
    sum += numArr[i];
  }

  return sum / numArr.length;
}

// averageNum([1, 2, 3, 4, 5 ,6, 7, 8, 9]);

/* 
  psuedo + notes:
  write function that accepts an array of integers and returns the average numbe

  input: array of integers
  output: integers

  ex: averageNum([1, 2, 3]) ==> return 2
  1. declare int variable to zero to be used with loop
  2. write loop that iterates and adds to sum variable
  3. return the sum divided the length of the array
*/

// ******* QUESTION 2 *******
// Write a method or function that takes an array of strings and returns the difference in length between the shortest and longest string in the array.

const strLengthDifference = strArr => {
  let sortedArr = strArr.sort((a, b) => b.length - a.length)

  const lowest = sortedArr[sortedArr.length - 1].length;
  const longest = sortedArr[0].length;

  return longest - lowest;
} 

strLengthDifference([ "bb", "dddd", "a", "ccc"])

/* 
  psuedo + notes:
  input: array of string
  output: integer

  strLengthDifference(["a", "bb", "ccc", "dddd"]) ==> return 3

  1. first sort arr by length using sort method
  2. declare two variables, lowest & highest, and set to the beginning of array and to the end of array by index
  3. return difference of length of both variables
*/

// ******* QUESTION 3 *******
// Write a method that takes two numbers and returns true if the greatest common denominator of the two numbers is even and false if it is odd.

function findGCD(n1, n2){
  let smaller = Math.min(n1, n2);
  let larger = Math.max(n1, n2);

  if (larger % smaller === 0){
    return smaller
  } else {
    return findGCD(smaller, larger % smaller)
  }
}

function isGCDEven(n1, n2){
  let gcd = findGCD(n1, n2)

  if (gcd % 2 === 0){
    return true;
  } else {
    return false;
  }
}

/* 
  psuedo + notes:
  input: two numbers
  output: boolean

  isGCDEven(10, 5) ==> return false;

  1. declare a smaller num variable and a larger num variable, use Math.min + Math.max 
  2. recursive solution, the termination block:
    if the remainder of the larger num divided by smaller num is zero (equally divided), then return smaller var
  3. or else, return gcd function 
*/

```
