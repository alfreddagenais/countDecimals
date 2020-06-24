# Javascript Count Decimals

A pure vanilla Javascript way to count decimals of a number

```javascript
countDecimals(0)    // => 0
countDecimals(1)    // => 0
countDecimals(1.1)  // => 1
countDecimals(1.11) // => 2
countDecimals(1/3)  // => 16

// Scientific notation is not supported.
countDecimals(1.1e-7) # => 4
```

### Benchmark

The implementation uses `String#indexOf` (faster ops/sec) instead of `String#split`.

That's with a modulo check (~4x faster for whole numbers).