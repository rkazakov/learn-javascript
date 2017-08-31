# Currying #

```
const add = (a, b) => a + b;

console.log(add(3, 5));

const addCurried = (a) => (b) => a + b;

console.log(addCurried(3)(5));

const add3 = addCurried(3);

console.log(add3(5));
```
