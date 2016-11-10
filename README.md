# ES6 Style Guide
An opinion on code style for ES6.  These are not rules to die over, but using them frequently will give a team the ability to read and understand code better.

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

Booleans and functions which return booleans should be prefaces with "be" conjugations.  
```es6
// GOOD
isOpen = false
isValid() // returns bool

// BAD
open = false
valid() // returns bool
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

## Functions
Callbacks should usually be arrow functions `=>`.
```es6
const fooIds = foos.map((foo) => foo.id);
```

But large callbacks should be defined outside, and passed in, when possible.
```
const foodBars = foos.reduce(getFooBars, []);

const getFooBars = (fooBars, foo) => {
  // computation for foo bars
  
  fooChildren.push(fooBar);
};
```

## Testing with Mocha
`describe`s describe things.  `context`s describe situations.  `it`s describe expected results.
