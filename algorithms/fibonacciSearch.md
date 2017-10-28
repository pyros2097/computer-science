# Fibonacci

https://en.wikipedia.org/wiki/Fibonacci_search_technique

1. Fibonacci using While Loop **Space Constant, Time O(n)**
```js
const fibonacci = (num) => {
  let a = 1, b = 0, temp;
  while (num >= 0 ) {
    temp = a;
    a = a + b;
    b = temp;
    num--;
  }
  return b;
}
```

2. Fibonacci Recursive **Space O(n), Time O(2^n)**
```js
const fibonacci = (num) => {
  if (num <= 1) {
    return 1;
  }
  return fibonacci(num - 1) + fibonacci(num - 2);
}
```

3. Fibonacci Memoization **Space O(n), Time O(2n)**
```js
const memo = {};
const fibonacci = (num) => {
  if (memo[num]) {
    return memo[num]
  };
  if (num <= 1) {
    return 1;
  }
  memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);
  return memo[num];
}
```

4. Fibonacci Fastest **Space O(1), Time O(1)**
```js
const fibonacci = (n) => {
 return Math.round((Math.pow((1 + Math.sqrt(5)) / 2, n) —  Math.pow(-2 / (1 + Math.sqrt(5)), n)) / Math.sqrt(5));
}

```

5. Fibonacci Dynamic Programming
```js
const fibonacci = (n, i = 0, a = 0, b = 1) => {
  if (i < n) {
    return fibonacci(n, i + 1, b, a + b);
  }
  return b;
}
```