1 Print Odd Numbers in an Array (using anonymous function):


const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];

numbers.forEach(function (number) {
  if (number % 2 !== 0) {
    console.log(number);
  }
});

2 Convert All Strings to Title Caps in a String Array (using anonymous function):

const strings = ["hello", "world", "javascript"];

const titleCaps = strings.map(function (str) {
  return str.charAt(0).toUpperCase() + str.slice(1);
});

console.log(titleCaps);

3 Sum of All Numbers in an Array (using anonymous function):

const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce(function (acc, curr) {
  return acc + curr;
}, 0);

console.log(sum);

4 Return All Prime Numbers in an Array (using anonymous function):


function isPrime(num) {
  if (num <= 1) return false;
  if (num <= 3) return true;

  if (num % 2 === 0 || num % 3 === 0) return false;

  for (let i = 5; i * i <= num; i += 6) {
    if (num % i === 0 || num % (i + 2) === 0) return false;
  }

  return true;
}

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];

const primeNumbers = numbers.filter(function (number) {
  return isPrime(number);
});

console.log(primeNumbers);

5 Return All Palindromes in an Array (using anonymous function):

function isPalindrome(str) {
  const reversed = str.split("").reverse().join("");
  return str === reversed;
}

const strings = ["racecar", "hello", "level", "world"];

const palindromes = strings.filter(function (str) {
  return isPalindrome(str);
});

console.log(palindromes);


6 Return Median of Two Sorted Arrays of the Same Size (using anonymous function):

function findMedianSortedArrays(nums1, nums2) {
  const merged = nums1.concat(nums2).sort((a, b) => a - b);
  const length = merged.length;
  
  if (length % 2 === 0) {
    return (merged[length / 2 - 1] + merged[length / 2]) / 2;
  } else {
    return merged[Math.floor(length / 2)];
  }
}

const arr1 = [1, 3, 5];
const arr2 = [2, 4, 6];

console.log(findMedianSortedArrays(arr1, arr2));

7 Remove Duplicates from an Array (using anonymous function):

const numbers = [1, 2, 2, 3, 4, 4, 5, 5];

const uniqueNumbers = numbers.filter(function (value, index, self) {
  return self.indexOf(value) === index;
});

console.log(uniqueNumbers);


8 Rotate an Array by k Times (using anonymous function):

function rotateArray(arr, k) {
  const n = arr.length;
  k %= n;
  const rotated = arr.slice(k).concat(arr.slice(0, k));
  return rotated;
}

const numbers = [1, 2, 3, 4, 5];
const k = 2;

console.log(rotateArray(numbers, k));

