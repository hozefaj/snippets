## Javascript

* Arrays
* `typeOf`

###[Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

1. [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) to loop through array
2. [filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) to remove elements from array
3. [map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) to modify array and store into a new array
4. [reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce) to compare elements within the array
5. [slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) returns a shallow copy of a portion of an array into a new array object

```javascript
// create array
var list = [1, 
        'string', 
        { type: true }, 
        [1,2,3], 
        function(){console.log("function within an array")}
      ];

// push the begining of array
list.unshift('at the beginning');
// get first item in the array
var firstitem = list.shift();

// push at end of array
list.push(at the end);
//get the last item in the array
var lastitem = list.pop();

// loop through the array & perform operation
list.forEach(function(item) {
  console.log(item);
});

// filter out elements from array
list.filter(function(item) {
        if(item === <something>) return false;
        return true;
});

// modify the array
list = list.map(function(item){
        // do something
        return item;
});

// reduce the array....get an element based on some condition
var someItem = list.reduce(fucntion(previousValue, currentValue) {
        // some example code
        if(previousValue > currentValue) return previousValue;
        return currentValue;
})
```

###Figuring out what something is...

```javascript
// using typeOf and instanceOf
var a = 3;
console.log(typeof a); // number

var b = "Hello";
console.log(typeof b); // string

var c = {};
console.log(typeof c); // object

var d = []; 
console.log(typeof d); // object (not an array)
console.log(Object.prototype.toString.call(d)); // array

function Person(name) {
    this.name = name;
}

var e = new Person('Jane');
console.log(typeof e); // object
console.log(e instanceof Person); // true

console.log(typeof undefined); // undefined....makes sense
console.log(typeof null); // object....a bug since, like, forever...

var z = function() { };
console.log(typeof z); // function....since its a first class function
```


