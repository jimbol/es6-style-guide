# ES6 Style Guide
An opinion on code style for ES6

## Labeling Variables
An id should always include the term `Id`
```es6
// GOOD
itemId
personId

// BAD
item
person
```

Functions should always be verbs or questions
```es6
// GOOD
switchValue()
isValid()

// BAD
value()
valid()
```

Top level constants should be all caps underscore case
```es6
// GOOD
const OPEN_ID = 'OPEN_ID';

function isOpen() {
  const openId = getCurId(); // function level `const`s are treated normally
  return openId === OPEN_ID;
}

// BAD
const openId = 'OPEN_ID';
```
