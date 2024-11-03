
### Nullish coalescing (??)
In JavaScript, developers have often used the logical OR (||) operator to assign default values when a variable is undefined or null. However, this can behave unexpectedly when the variable holds values like 0, false, or an empty string (""), because || treats them as falsy and substitutes the default value.

```javascript
const result = value || 10;

// Nullish coalescing
const result = value ?? 10;
```

### Optional chaining
When dealing with deeply nested objects or arrays, it's common to have to check whether each property or array element exists before trying to access the next level. Without optional chaining, this requires verbose and repetitive code.

```javascript

// Without optional chaining
const tax = (product.price && product.price.tax) ?? undefined;

const tax = product?.price?.tax;

```


### Interaction with object keys and values

```javascript
const obj = { a: 1, b: 2, c: 3 };

// Using Object.entries() to iterate over key-value pairs
Object.entries(obj).forEach(([key, value]) => {
  console.log(key, value);
});

// Using Object.values() to work directly with values
Object.values(obj).forEach(value => {
  console.log(value);
});
```

### Check the array type of a variable
```javascript
const arr = [1, 2, 3];
console.log(Array.isArray(arr)); // true
```


### Working with number please these libraries
[Article](https://blog.jetbrains.com/webstorm/2024/10/javascript-best-practices-2024/#dont-use-built-in-number-for-sensitive-calculations)
 
- [decimal.js](https://mikemcl.github.io/decimal.js/)
- [big.js](https://mikemcl.github.io/big.js/)



(Articel link)[https://blog.jetbrains.com/webstorm/2024/10/javascript-best-practices-2024/?ref=dailydev]