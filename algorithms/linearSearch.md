# Linear Search **Time O(n)**

```js
const linearSearch = (arr, key) => {
  for (let i = 0; i < arr.length; i++) {
    const item = arr[i];
    if (item === key) {
      return i;
    }
  }
  return -1;
}
```