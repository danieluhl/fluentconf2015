## Day 1

Excited to arrive in SF, got upgraded to an awesome top floor king 1 bedroom suite! Looking forward to learning a lot and networking with the best at fluent!

## Morning Networking

Going really well


## ES6 Training Class
@raushma
@js_dev
#FluentConf

### Origins
- EcmaScript vs JavaScript
- Originally Sun now Oracle TM JavaScript
- Now ES2015

Go playing at the same time, lolz

### Using ES6
- ASM js
- No engine currently fully supports ES6
- ES6 must not have breaking changes
- TC39 did a really good job given their constraints
- Design by committee is a real danger


### Design by Champions!

### Transpile
- New features are almost impossible to transpile
- Better library features are easy
- ES6 is done, the spec is frozen
- in June there will be a formal publication
- kangax es6 feature table

### ES6 Now!

- jspm
- systemjs
- core.js
- es6-shim

### Features!

- For let, transpilers will rename the variable (this might make it hard to track in code if it obfuscates)
- Might just do myVar, myVar_1, etc.
- Destructuring - variable declarations, assignments, parameter definitions

    let {first: f, last: l} = obj

- ...rest

    let [x, y, ...rest] = ['a', 'b', 'c', 'd'];

- regex

    let [all, year, month, day] = 'my sweet regex'.exec('something')

- multiple return values

### Modules

- only loaded when needed
- don't pollute the global namespace
- you can pull any export by name from a library - partial loading of single modules?
- does importing one function only import the function, or does the entire module with all exports get downloaded?
- shortcut:

    export default function(...){...}
    ...
    import default function


## Live Coding (because no internet)

- jest (facebook)
- pull this repo and give this talk for wf
- random curlies will now make a difference

jest.autoMockOff()
xit()

- destructuring an invalid value gives you undefined (not throw an error!)
- we would want to statically check for this issue somehow^^

    let {coords:{lat, long}} = getAddresss(); // coords = undefined (only right side vars matter)

- lhs can get crazy, use tricks to filter the values you want from your object rather than fighting the left hand side

git clone https://github.com/aaronfrost/es6-workshop

### Break

### Back to the icy arctic that is the front row of salon 9

- using my laptop for warmth
- computed property keys
- default parameter values

    function func2(arg0, ...others) {
        return others;
    }

- NEVER USE ARGUMENTS anymore (do we still need apply then?)
- args with others is an array!
- named parameters!
- crockford looks like the god of javascript

    foo({x: 2, y: 3});
    function foo({y=1, x=0, z=0}) {
        ...
    }

- Here the function destructures the object literal and uses default values when something is missing

### Spread

- Splits all elements in an array

    Math.max(...[7, 8, 9]);

### Arrow functions

- parameter => function

    arr.map(a => a * a);

- arrow function "this" keyword works appropriately

    button.addEventListener('click', () => {
        this.handleClick(); //yup, this is what you would expect here
    });

- no more self=this!
- multi param arrow functions (this, that) => {stmt1; stmt2;}

- null bypasses default parameter values in functions

    function myFunction({name='dan', age=30, favoriteBand=false}={}){

- everything is optional
- object literal with arrow functions
- object literal with functions

### Classes

- new syntax
- no commas
- more portable code (common inheritance api)
- tooling (ides, type checkers, etc)
- immutable objects (your own primitaves)
- traits (similar to mixins)
- subclassing built-ins (validation)
- help newcomers learn the language

- Template literals

    let str = `this is
    a text with
    multiple lines`;

- lnrs:

    foo`Hello ${first}`
    // shorthand for
    foo(['Hello', ' '], first);

- web templates are data
- template literals are code (multi string literals plus interpolation)
- tagged templates are code (function calls)
- XRegExp library

- JSX as part of the language via tagged templates
- Maps
- sweet object keys

### weak maps WeakMap()

- weak maps - construct for private data
- the key is not prevented from gc
- weak maps have values removed when references are lost like normal gc works
- use pattern where instead of a local closure you use a weak map for a single piece of
data used by a object

### Iterators and Generators

iteratable
- Arrays, strings, maps, sets, arguments, dom data structures (not plain objects)

iterating constructs
- Destructuring, for-of, array.from, spread, constructor of maps, promise.all, yield

for-of is a better for loop (replaces array.foreach)

### Set

slideshare.net/jpamental
github.com/jpamental


# React (es6 react best practices)

- Brian Holt @holtbt
- react - you can use it with backbone, but don't
- reacts greatest contribution is one way data flow
- state is the enemy o fthe maintainable app
- use props as much as you can (props are immutable)
- drilling holes (pass the child a callback on the parent)

### dealing with data in react

- it's up to you
- it's hard to play with angular from outside angular
- it's easy to have a react component on your backbone page
- it's easy to get away from react?

#### mini cart example

- communicating between components
- event bus
- don't try to sync state (it's impossible)
- you need a single source of truth
- flux is overkill for anything but a giant app

### react with js6

- babel has jsx built-in
- using koa instead of express for generators in our middle layer
- jest is on jasmine 1.3 - mocha uses jasmine 2.x
- always assume all of your data is already there (typically by props)

- container layout paradigm - separate behavior from layout then just feed the layout into the behavior

- container has all the logic, 2 layouts use the container (list, tile)
- all react tags can be self closing












































