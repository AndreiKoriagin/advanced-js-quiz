What happens if we run this code sample?

```ecmascript 6
String.prototype.givePizza = function() {
    console.log('give ' + this + ' pizza!');
};

const name = 'John';

name.givePizza();

```

1. Error assigning `givePizza` function
2. Error calling `name.givePizza()` 
3. `give John pizza!` printed
4. `give undefined pizza!` printed

correct answer: 3.

***

Expected output:

```ecmascript 6
var hero = {
    _name: 'Tony Stark',
    getIdentity: function (){
        return this._name;
    }
};
var heroIdentity = hero.getIdentity;

console.log(heroIdentity());
console.log(hero.getIdentity());
```

1. `Tony Stark`, `Tony Stark`
2. `Tony Stark`, `undefined`
3. Runtime error
4. `undefined`, `undefined`

correct answer: 2.

***

Expected output:
```ecmascript 6
let i;
for (i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 0);
}

```

1. No output
2. `0 1 2`
3. `1 2 3`
4. `3 3 3`

Correct answer: 4.

***

Expected output:

```ecmascript 6
setTimeout(() => console.log('timeout'), 0);

Promise.resolve('resolve')
    .then(()) => console.log('1st then'))
    .then(()) => console.log('2nd then'));

console.log('simple console log');
```

Answer: 
- `simple console log`
- `1st then`
- `2nd then`
- `timeout`

***

Expected output:
```ecmascript 6
let someString = 'react';
someString[0] = 'R';
console.log(someString);
```

1. `React`
2. `react`
3. `eact`
4. Runtime error

Correct answer: 2;

***

Expected output:

```ecmascript 6
const x = 42;

if (x > 4) {
  console.log(x);
  let x = 10;
}
```

1. ReferenceError: Cannot access 'x' before initialization
2. `42`
3. `10`
4. ReferenceError: x is not defined

Correct answer: 1.

***

Expected output:

```ecmascript 6
const x = 5;

if (x > 4) {
  setTimeout(() => console.log(x), 0);
  let x = 10;
}
```

1. ReferenceError: Cannot access 'x' before initialization
2. `42`
3. ReferenceError: x is not defined
4. `10`

correct answer: 4.

***

Expected output:

```ecmascript 6
    doSomething();

    let doSomething() = function() { /* implementation */ }
```

1. Runs successfully
2. Reference error

Correct answer: 2.

***

Expected output:

```ecmascript 6
    doSomething();

    function doSomething() { /* implementation */ }
```

1. Runs successfully
2. Reference error

Correct answer: 1.

***

Expected output:

```ecmascript 6
const someObj = {};
someObj[1] = 5;

console.log(someObj['1']);
```

1. `undefined`
2. Runtime error
3. `5`
4. `null`

correct answer: 3.

***

Expected output:

```ecmascript 6
const someObj = {};
someObj[{}] = 42;

console.log(someObj[{}]);
```

1. `undefined`
2. `42`
3. Runtime error
4. `null`

correct answer: 2.

***

Expected output:

```ecmascript 6
const someObj = {};
someObj[{}] = 42;

console.log(someObj[{ id: 42 }]);
```

1. `undefined`
2. Runtime error
3. `42`
4. `null`


correct answer: 3.

***

Expected output:

```ecmascript 6
const someObj = {};
someObj['true'] = 500;


console.log(someObj[true]);
```

1. `500`
2. `undefined`
3. Runtime error
4. `null`

correct answer: 1.

***

Expected output:

```ecmascript 6
const someArray = [];

someArray[10] = 5;
console.log(someArray.length);
```

1. `10`
2. `11`
3. `1`
4. `2`

Correct answer: 2.

***

Expected output:

```ecmascript 6
var hero = {
    name: 'Iron Man',
    sayName: () => {
        console.log(this.name);
    }
}
```

1. `Iron Man`
2. `undefined`
3. Runtime error
4. Reference error

Correct answer: 2.

***

Expected output if the `button` is clicked:

```html
<div onclick="console.log('first-div')">
  <div onclick="console.log('second-div')">
    <button onclick="console.log('button')"></button>
  </div>
</div>
```

Correct answer: button, second-div, first-div.

***

Expected output:

```ecmascript 6
console.log(Symbol('test') === Symbol('test'));
```

answer: false;

***

Expected output:

```
function prepareActionWith(action, a) {
    return (b) => action(a, b);
}

function sum(a, b) {
    return a + b;
}

const useWithFive = prepareActionWith(sum, 5);
console.log(useWithFive(3));
```

answer: `8`.

***

Expected output:

```
Object.prototype.toString = function() {
    return this.value;
}

const obj = {value: 42};

console.log(obj == '42');

```

Answer: `true`.