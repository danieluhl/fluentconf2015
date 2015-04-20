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











































