# Exponential Search **Time O(log i)**

This is because exponential search will run in O(log i) time, where i is the index of the element being searched for in the list, whereas binary search would run in O(log n) time, where n is the number of elements in the list.

Exponential search allows for searching through a sorted, unbounded list for a specified input value (the search "key"). The algorithm consists of two stages. 
1. The first stage determines a range in which the search key would reside if it were in the list. Assuming that the list is sorted in ascending order, the algorithm looks for the first exponent, j, where the value 2j is greater than the search key. This value, 2j becomes the upper bound for the binary search with the previous power of 2, 2j - 1, being the lower bound for the binary search.[3]
2. In the second stage, a binary search is performed on this range. 

```js
const exponentialSearch = (arr, key) => {
  let bound = 1;
  while (bound < arr.length && arr[bound] < key) {
      bound *= 2;
  }
  return binarySearch(arr, key, bound/2, Math.min(bound, arr.length));
}
```