# JavaScript Basics 

Based on [JavaScript in 3 hours from freeCodeCamp.org](https://www.youtube.com/watch?v=PkZNo7MFNFg)

1. Web Browser

```html
<script>
  console.log("hello world");
</script>
```

Tip: Open Console: `Ctrl+Shift+J`

2. https://www.freecodecamp.org/
3. https://codepen.io/ (code playground)

### Comments:

```js
// in-line comment
/* multi-line comment
*
*/ 
```

### Data Type and Variables:

```js
/* Data Types:
undefined, null, boolean, string, symbol, number, and object
*/

/* Variable: 
var myName = "Ehsan" --> will use in the whole
let myName = "Ehsan" --> in some part
const pi = 3.14 --> should never changed, and can't as well
*/
```

### Storing values with Assignment Operator:

```js
/*
Declaration --> var a;
Assignment --> var b = 2;

var b = a;
*/
```

### Console:

`console.log()` --> see things in console

### Initializing Variables w/ Assignment Operator:

```js 
var a = 9;
```

### Uninitializing Variables:

```js 
a = a + 1; 
```

### Case Sensivity in Variables:

```js 
camelCase --> myName 
```

### Numbers:

```js
Adding --> var sum = 10 + 10;
Subtracting --> var difference = 44 - 23;
Multiplying --> var product = 10 * 2;
Dividing --> quotient = 66 / 13;
Incermenting --> var myVar = 87; myVar = myVar + 1; --> myVar++;
Decrementing --> myVar = myVar - 1; --> myVar--;
Decimal --> var a = 0.0009;
Multiply Decimal --> var b = 2.4 * 3.9;
Divid Decimal --> var c = 3.3 / 1.6;
Reminder --> var reminder; reminder = 11 % 3; --> a number is even or odd
```

### Compound Assignment with Augmented ...:

```js
a = a + 12; --> a += 12;
b += 9;

a -= 12;

a *= 9;

a /= 10;
```

### Declare Storing Variables:

```js
var myName = "Ehsan"
var myName = 'Ehsan'
```

### Escaping Literal Quotes in Strings:

```js
var myStr = "I am a \"double quoted\" string inside \"double quotes\""
```

### Quoting Strings with Single Quotes:

```js
var myStr = 'I am a "double quoted" string inside "double quotes"'
```

### Escape Sequences in Strings:

```js
/*****
CODE      OUTPUT
\'        single quote
\"        double quote
\\        backslash
\n        newline
\r        carriage return
\t        tab
\b        backspace
\f        form feed
*****/
```
```js
var myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
```

### Concatenating Strings with Plus Operator:

```js
var ourStr = "I come first ." + "I come next";
```

### Concatenating Strings with Plus Equals Operator:

```js
var ourStr = "I come first. ";
ourStr += "I come second";
```

### Constructing Strings with Variables:

```js
var theName = "Ehsan";
ourStr = "Hello " + theName + ", how are you?";
```

### Appending Variables to Strings:

```js
var ajective = "awesome";
var ourStr = "Ehsan is ";
ourStr += ajective;
```

### Find length of String:

```js
var firstNameLength = 0;
var firstName = "Ehsan";
firstNameLength = firstName.length;
```

### Bracket Notation to Find First Character in Storing:

Java script is based on zero-based indexing (starts from 0)

```js
firstLatterOfFirstName = "";
var firstName = "Ehsan";

firstLatterOfFirstName = firstName [0];
```

### String Immutability:

```js
var myStr = "Jello World";
myStr[0] = "H";

myStr = "Hello World";
```

### Bracket Notation to Find Last Character in String:

```js
var firstName = "Ehsan";
var lastLetterOfFirstName = firstName[firstName.length - 1];
```
```js
/**
* Noun
* Verb
* Adjective
* Adverb
*/
```

### World Blanks:

```js
function worldBlanks(myNoun, myAdjective, myVerb, myAdverb) {
var result = "";
result += "The " + myAdjective + " " + myNoun + " " + myVerb + " to the store " + myAdverb;
return result;
}

console.log(worldBlanks("dog", "big", "ran", "quickly"));
```

### Store Multiple Values with Arrays:

```js
/* Arrays allow us to store several pieces of data in one place */

var ourArray = ["Ehsan", 36, "Zanjan", "Iran"]
```

### Nested Arrays:

The array inside other array called "Nested Array" or "Multi-Dimensional Array"

```js
var ourArray = [["the universe", 42], ["everything", 101010]];
```

### Access Array Data with Indexes:

```js
var ourArray = [50, 60, 70];
var ourData = ourArray[0]; // equals 50
```

### Modify Array with Indexes:

```js
var ourArray = [18, 64, 99];
ourArray[1] = 52; // ourArray now equals [18, 52, 99]
```

### Access Nested-Arrays with Indexes:

```js
var ourArray = [[1, 2, 3], [4, 5, 6], [7,8,9], [[10, 11, 12], 13, 14]]; // three-layer deep array
var myData = ourArray[0][0];
```

### Manipulate Arrays with `push()`:

Adds the array to the end

```js
var ourArray = [1, 2, 3];
ourArray.push([4, 5]); // ourArray now equals [1, 2, 3, [4, 5]]
```

### Manipulate Arrays with `pop()`:

Removes the last array

```js
var ourArray = [1, 2, 3];
ourArray.pop(); // ourArray now equals [1, 2]
```

### Manipulate Arrays with `shift()`:

Removes the first array

```js
var ourArray = [1, 2, 3];
ourArray.shift(); // ourArray now equals [2, 3]
```

### Manipulate Arrays with `unshift()`:

Adds the array to the beginning

```js
var ourArray = [1, 2, 3];
ourArray.push([4, 5]); // ourArray now equals [[4, 5], 1, 2, 3]
```

### Shopping List (Nester Arrays):

```js
var myList = [["cereal", 3], ["milk", 2], ["bananas", 3], ["juice", 2], ["egges", 12]];
```

### Write Reusable Code with Functions:

```js
function ourReusableFunction() {

}

ourReusableFunction();
```

Every time the function is called it will run the reusable code inside it

### Passing Values to Functions with Arguments:

```js
/* Parameters are variables that act as placeholders for the values that are to be input to a function when it is called */

function ourFunctionWithArgs(a, b) {
console.log(a - b);
}

ourFunctionWithArgs(10, 5);
```

### Global Scope and Functions:

```js
/* Scope refers to the visibility of variables 
* Global Scope means it can be seen everywhere in our JS code
*/

var myGlobal = 10;

function fun1() {

  oopsGlobal = 5; // it doesn't have var, so it becomes global automatically

}

function fun2() {

var output = "";
if (typeof myGlobal != "undifined") {
output += "myGlobal: " + myGlobal;
}
if (typeof oopsGlobal != "undifined") {
output += " oopsGlobal: " + oopsGlobal;
}
console.log(output);
}

fun1;
fun2;
```

### Local Scope and Functions:

```js
function myLocalScope() {
var myVar = 10;
console.log(myVar);
}

console.log(myVar); // this one gives ERROR because myVar is local
```

### Global vs. Local in Functions:

```js
var outWear = "T-Shirt"; // Global

function myOutfit() {
  var outWear = "Sweater"; // Local
  return outWear;
}

console.log(myOutfit()); // Sweater
console.log(outWear); // T-Shirt
```

### Return a Value from a Function with Return:

```js
function minusSeven(num) {
  return num - 7;
}

console.log(minusSeven(10));
```

### Assignment with a Returned Value:

```js
var changed = 0;
function changedArg(num) {
  return (num + 5) / 3;
}

changed = changedArg(10);
```

### Stand in Line:

```js
function nextInLine(arr, item) {
  arr.push(item);
  return arr.shift();
}

var testArr = [1, 2, 3, 4, 5];

console.log("Before: " + JSON.stringify(testArr)); // `JSON.stringify(testArr)` converts array to string
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```

### Bolean (True or False) Values:

```js
function x() {
return false;
}
```

### Use Conditional Logic with If Statements:

```js
/* If used to make decisions in code */

function ourTrueOrFalse(isItTrue) {
  if (isItTrue) {
    return "Yes, it's true";
  }
    return "No, it's false";
}

console.log(ourTrueOrFalse(true));
```

### Comparison with the Equality Operator:

```js
function testEqual(val) {
  if (val == 12) // = is asignment and == is equal
    return = "Equal";
}
    return = "Not Equal";

console.log(testEqual(10));
```

### Comparison with the Strict Equality Operator:

```js
/*
3 === 3 is true
3 === '3' is false

because == converts types but === is strict and doesn't convert types
*/
```

### Comparison with the Inequality Operator:

```js
3 != 4
3 !== '3'
```

### Comparison with the Logical And Operator:

```js
if (val > 10) {} // Greater than
if (val < 10) {} // Less than
if (val >= 10) {} // Greater than or equal
if (val <= 10) {} // Less than or equal
```
```js
if (val <= 50) {
  if (val >= 20) {
    return "Yes";
}
   return "No";
```
```js  
if (val <= 50 && val >= 25) {}  // And Operator
if (val < 10 || val > 20) {}  // Or
```

### Else Statements:

```js
function testElse(val) {
  if (var > 5) {
    result = "Bigger than 5";
} else {
    result = "5 or smaller"
}
  return result;
}
```

### Else If Statements:

```js
if (val > 10) {
  return "Greater than 10";
} else if (val < 5) {
    return "Smaller than 5";
} else {
    return "Between 5 and 10";
}
```

### Logical Order in If Else Statements:

```js
/* Order matters, so put statements in the correct way
for instance:
first check (val < 10)
then check (val <5)
*/
```
```js
/*
n < 5 : "Tiny"
n < 10 : "Small"
n < 15 : "Medium"
n < 20 : "Large"
n >= 20 : "Huge"
*/

function testSize(num) {
  if (num < 5) {
    return "Tiny";
  } else if (num < 10) {
    return "Small";
  } else if (num < 15) {
    return "Large";
  } else {
    return "Huge";
  }
}

console.log(testSize(19));
```

### Golf Code:

```js
var names = ["Hello-in-One!", "Eagle", "Birdie", "Par", "Bogey", "Doule Bogey!", "Go Home!"]

function golfScore(par, strokes) {
  if (strokes == 1) {
    return names[0];
  } else if (strokes <= par - 2) {
    return names[1];
  } else if (strokes == par - 1) {
    return names[2];
  } else if (strokes == par) {
    return names[3];
  } else if (strokes == par + 1) {
    return names[4];
  } else if (strokes == par + 2) {
    return names[5];
  } else if (strokes >= par + 3) {
    return names[6];
  }
}

console.log(golfScore(4, 3));
```

### Switch Statements:

```js
function caseInSwitch(val) {
  var answer = "";
    switch(val) {
	  case 1:
	    answer = "Alpha";
		  break;
	  case 2:
	    answer = "Beta";
		  break;
	  case 3:
	    answer = "Gamma";
		  break;
	  case 4:
	    answer = "Delta";
		  break;
	}
  return answer;
}

console.log(caseInSwitch(1));
```

### Defult Option in Switch Statements:

```js
function caseInSwitch(val) {
  var answer = "";
    switch(val) {
	  case 1:
	    answer = "Alpha";
		  break;
	  case 2:
	    answer = "Beta";
		  break;
	  case 3:
	    answer = "Gamma";
		  break;
	  case 4:
	    answer = "Delta";
		  break;
	  default:
	    answer = "Stuff";
		  break;
	}
  return answer;
}

console.log(caseInSwitch(10));
```

### Replacing If Else Chains with Switch:

```js
/* sometimes we can replace ifs and else ifs with switches */
```

### Returning Boolean Values from Functions:

```js
function isLess(a, b) {
  return a < b;
}

console.log(isLess(10, 15));
```

### Counting Cards:

```js
var count = 0;

function cc(card) {
  switch(card) {
    case 2:
	case 3:
	case 4:
	case 5:
	case 6:
	  count++;
	    break;
    case 10:
	case "J":
	case "Q":
	case "K":
	case "A":
	  count--;
	    break;
  }
  
  var holdbet = 'Hold'
    if (count > 0) {
	  holdbet = 'Bet'
	}
  
  return count + " " + holdbet;
}

cc(2); cc('K'); cc(10); cc('K'); cc('A');

console.log(cc(4));
```

### Build Javascript Objects:

```js
/* Objects are like arrays but has Properties */

var ourDog = {
  "name": "Jully",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};
```

### Accessing Object Properties with Dot or Bracket notation:

```js
var dogName = ourDog.name;
var dogLegs = ourDog.legs;
```
```js
/* Bracket used when the properties have space */

var testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};

var entreeValue = testObj["an entree"]
var drinkValue = testObj['the drink']
```

### Accessing Object Properties with Variables:

```js
var testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};

var playerNumber = 16;
var player = testObj[playerNumber];
```

### Updating Object Properties:

```js
var ourDog = {
  "name": "Jully",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.name = "Hanni";
```

### Add New Properties to an Object:

```js
ourDog.bark = "Woof";
or
ourDog["bark"] = "Woof";
```

### Delete Properties from an Object:

```js
delete ourDog.bark;
```

### Using Objects for Lookups:

```js
function phoneticLookup(val) {
  var result = "";
  
  var lookup = {
    "alpha": "Adams",
	"bravo": "Boston",
	"charlie": "Chicago",
	"delta": "Denver",
  };
  
  result = lookup[val];
  
  return result;
}

console.log(phoneticLookup("charlie"));
```

### Testing Objects for Properties:

```js
var myObj = {
  gift: "pony",
  pet: "kitten"
  bed: "sleigh"
};

function checkObj(checkProp) {
  if (myObj.hasOwnProperty(checkProp)) {
    return myObj[checkProp];
  } else {
    return "Not Found";
  }
}

console.log(checkObj(gift));
```

### Manipulating Complex Objects:

```js
var myMusic = [
  {
    "artist": "Billy Joel",
	"title": "Piano Man",
	"release_year": 1973,
	"formats": [
	  "CD",
	  "8T",
	  "LP"
	]
	"gold": true
  }
  {
    "artist": "Beau Carnes",
	"title": "Cereal Man",
	"release_year": 2003,
	"formats": [
	  "YouTube Video",
	  "DVD"
	]
	"gold": true
  }
];
```

### Accessing Nested Objects:

```js
var myStorage = {
  "car": {
    "inside": {
	  "glove box": "maps",
	  "passenger seat": "crumbs"
	},
    "outside": {
      "trunk": "jack"
	}
  }
};

var gloveBoxContents = myStorage.car.inside["glove box"];
console.log(gloveBoxContents);
```

### Accessing Nested Arrays:

```js
var myPlants = [
  {
    type: "flowers",
	list: [
	  "rose",
	  "tulip",
	  "dandelion"
	]
  },
  {
    type: "trees",
	list: [
	  "fir",
	  "pine",
	  "birch"
	]
  }
];

var secondTree = myPlants[1].list[1];

console.log(secondTree);
```

### Record Collection:

```js
var collection = {
  "2548": {
    "album": "Slippery When Wet",
	"artist": "Bon Jovi",
	"track": [
	  "Let It Rock",
	  "You Give Love A Bad Name"
	]
    },
  "2408": {
    "album": "1999",
	"artist": "Prince",
	"track": [
	  "1999",
	  "Little Red Corvette"
	]
    },
  "1245": {
	"artist": "Robert Palmer",
	"track": [ ]
    },
  "5439": {
    "album": "ABBA Gold"
	}
};

// Keep a copy of collection for test
var collectionCopy = JSON.parse(JSON.stringify(collection));

function updateRecords(id, prop, val) {
  if (val === "") {
    delete collection[id][prop];
  } else if (prop === "track") {
      collection[id][prop] = collection [id][prop] || [];
	  collection[id][prop].push(val);
  } else {
      collection[id][prop] = val;
  }
  
  return collection;
}

updateRecords(2408, "track", "test");
console.log(updateRecords(5439, "artist", "ABBA"));
```

### Interate with While Loops:

```js
var myArray = [];

var i = 0;
while (i < 5) {
  myArray.push(i);
    i++;
}

console.log(myArray);
```

### Interate with For Loops:

```js
var myArray = [];

for (var i = 0; i < 5; i++) {
  myArray.push(i);
}
```

### Interate Odd Numbers with For Loops:

```js
var ourArray = [];

for (var i = 1; i < 10; i += 2) {
  ourArray.push(i);
}

console.log(ourArray);
```

### Count Backwards with For Loops:

```js
var ourArray = [];

for (var i = 10; i > 0; i -= 2) {
  ourArray.push(i);
}

console.log(ourArray);
```

### Interate Through an Array with a For Loop:

```js
var ourArr = [9, 10, 11, 12];
var ourTotal = 0;

for (var i = 0; i < ourArr.length; i++) {
  ourTotal += ourArr[i];
}

console.log(ourTotal);
```

### Nesting For Loops:

```js
var product = multiplyAll([[1, 2], [3, 4], [5, 6, 7]]);

function multiplyAll(arr) {
  var product = 1;
  
  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < arr[i].length; j++) {
	  product *= arr[i][j];
	}
  }
  return product;
}

console.log(product);
```

### Interatee with `Do...While` Loops:

```js
var myArray = [];
var i = 10;

do {
  myArray.push(i);
  i++;
} while (i < 5)
```

### Profile Lookup:

```js
var contacts = [
{
  "firstName": "Akira",
  "lastName": "Laine",
  "number": "0543236543",
  "likes": ["Pizza", "Coding", "Brownie Points"]
},
{
  "firstName": "Harry",
  "lastName": "Potter",
  "number": "0994372684",
  "likes": ["Hogwarts", "Magic", "Hagrid"]
},
{
  "firstName": "Sherlock",
  "lastName": "Holmes",
  "number": "0487345643",
  "likes": ["Intriging Cases", "Violin"]
},
{
  "firstName": "Kristian",
  "lastName": "Vos",
  "number": "unknown",
  "likes": ["Javascript", "Gaming", "Foxes"]
}
];

function lookupProfile(name, prop) {
  for (var i = 0; i < contacts.length; i++) {
    if(contacts[i].firstName === name) {
	  return contacts[i][prop] || "No such property";
  }
  return "No such contact";
}

var data = lookupProfile("Akira", "likes");

console.log(data);
```

### Generating Random Fractions:

```js
function randomeFraction() {

return math.random();
}

console.log(randomeFraction());
```

### Generate Random Whole Numbers:

```js
var randomWholeNumberBetween0and19 = math.floor(math.random() * 20);

Generate Random Whole Numbers whithin a Range:

function ourRandomRange(ourMin, ourMax) {
  return math.floor(math.random() * (ourMax - ourMin + 1)) + ourMin;
}

ourRandomRange(1, 9);
```

### Use the parsInt Function:

```js
function convertToInteger(str) {
  return parsInt(str);
}

convertToInteger("56");
```

### Use the `parsInt` Function with a Radix:

```js
/* Radix specifies the base of a string. By default parsInt's base is 10 */

function convertToInteger(str) {
  return parsInt(str, 2);
}

convertToInteger("10011");
```

### Use the Conditionnal (Ternary) operator:

```js
/* condition ? statement-if-true : statement-if-false; */

function checkEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}

checkEqual(1, 2);
```
```js
function checkEqual(a, b) {
  return a ===b ? true : false;
}
```
Or
```js
function checkEqual(a, b) {
  return a ===b;
}
```

### Use Multiple Conditionnal (Ternary) operators:

```js
function checkSign(num) {
  return num > 0 ? "positive" : num < 0 ? "Negative" : "Zero";
}

checkSign(10);
```

### Difference Between var and `let` and `const` Keywords:

```js
/* let and const instead of var show errors if we want to override 
* however var is global and let is just in block
* when we use const the variable becomes read-only, so we can't assign it multiple times
*/
```

### Mutate an Array Declared with `const`:

```js
const s = [5, 7, 2];

function editInPlace() {
  "use strict";
  
  // s = [2, 5, 7]; won't work but bellow way works:
  
  s[0] = 2;
  s[1] = 5;
  s[2] = 7;
}

console.log(s);
```

### Prevent Object mutation:

```js
function freezObj() {
  "use strict";
  const MATH_CONSTANTS = { // this is a object block
    PI: 3.14
  };
  
  object.freez(MATH_CONSTANTS); // it freezes object and doesn't let we can change it
  
  try {  // with try-catch block we can change object block like const but ... see above!
    MATH_CONSTANTS.PI = 99;
  } catch(ex) {
    console.log(ex);
  }
  return MATH_CONSTANTS.PI;
}

const PI = freezObj();

console.log(PI);
```

### Use Arrow Functions to Write Concise Anonymous Functions:

```js
/* function without a name called anonymous function and it would be better write it as arrow function: () => */

var magic = function() { 
  return new date();
}

/* even we can shorten it if it just has one variable

const magic = () => new date();

*/
```

### Write Arrow Functions with Parameters:

```js
var myConcat = function(arr1, arr2) {
  return arr1.concat(arr2);
}
```
-->
```
const myConcat = (arr1, arr2) => arr1.concat(arr2);

console.log(myConcat([1, 2], [3, 4, 5]));
```

### Write Higher-Order Arrow Functions:

```js
const realNumberArray = [4, 5.6, -9.8, 3.14, 42, 6, 8.34, -2];

const squareList = (arr) => {
  const squaredIntegers = arr.filter(num => number.isInteger(num) && num > 0).map(x => x * x);
  return squaredIntegers;
};

const squaredIntegers = squareList(realNumberArray);
console.log(squaredIntegers);
```
```js
const increment = (function () {
  return function increment(num, val = 1) {
    return num + val;
  };
})();

console.log(increment(5, 3));
console.log(increment(5));
```

### Use the `rest` Operator with Function Parameters:

```js
const sum = (function() {
  return function sum(x, y, z) {
    const args = [x, y, z];
	  return args.reduce((a, b) => a + b, 0);
  };
}
)();
```
-->
```js
const sum = (function() {
  return function sum(...args) { // rest operator
	return args.reduce((a, b) => a + b, 0);
  };
}
)();

console.log(sum(1, 2, 3, 5, 6));
```

### Use the Spread Operator to Evaluate Arrays In-Place:

```js
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];

let arr2;
(function() {
  arr2 = [...arr1]; // copies all args of arr1
  arr1[0] = 'potato'
}
)();

console.log(arr2); // (5) ["JAN", "FEB", "MAR", "APR", "MAY"]
console.log(arr1); // (5) ["potato", "FEB", "MAR", "APR", "MAY"]
```

### Use Destructuring Assignment to Assign Variables from Objects:

```js
var voxel = {x : 3.6, y : 7.4, z : 6.54};

var x = voxel.x; // x = 3.6
var y = voxel.y; // y = 7.4
var z = voxel.z; // z = 6.54
```
-->
```js
const {x : a, y : b, z : c} = voxel; // a = 3.6, b = 7.4, z = 6.54 
```
```js
const AVG_TEMPERATURES = {
  today : 77.5,
  tomorrow : 79
}

function getTempOfTmrw(avgTemps) {
  const { tomorrow : tempOfTmrw} = avgTemps;
  return tempOfTmrw;
}

console.log(getTempOfTmrw(AVG_TEMPERATURES));

const LOCAL_FORECAST = {
  today: { min: 72, max: 83 },
  tomorrow: { min: 73.3, max: 84.6 }
};

function getMaxOfTmrw(forecast) {
  "use strict";
  
  const { tomorrow : { max: maxOfTmrw }} = forecast;
  
  return maxOfTmrw;
}

console.log(getMaxOfTmrw(LOCAL_FORECAST));
```

### Use Destructuring Assignment to Assign Variables from Arrays:

```js
const [z, x, , y] = [1, 2, 3, 4, 5, 6]; // z = 1, x = 2, y = 4 

let a = 8, b = 6;
(() => {
  "use strict";
  [a, b] = [b, a] // switchs the places
}
)();
```

### Use Destructuring Assignment with the Rest Operator:

```js
const source = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

function removeFirstTwo(list) {
  const [ , , ...arr] = list; // drops the first and second
  
  return arr;
}

const arr = removeFirstTwo(source);

console.log(arr);
console.log(source);
```

### Use Destructuring Assignment to Pass an Object as a Function's Parameters:

```js
const states = {
max: 56.78,
standard_devision: 4.34,
median: 34.54,
mode: 23.87,
average: 35.85,
min: -0.75
};

const half = (function() {
  
/*  return function half(states) {
    return (states.max + states.min) / 2.0; */
	
	return function half({max, min}) { // this is commonly used with APIs
    return (max + min) / 2.0;
  };
}
)();

console.log(states);
console.log(half(states));
```

### Create Strings using Template Litrals:

```js
const person = {
name: "Ehsan Azari",
age: 36
};

const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

console.log(greeting);
```
```js
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["id-blacklist", "no-dup-keys"]
};

function makeList(arr) {
  const resultDisplayArray = [];
  for (let i = 0; i < arr.length; i++) {
    resultDisplayArray.push(`<li class="text-warning">${arr[i]}</li>`)
  }
  
  return resultDisplayArray;
}

const resultDisplayArray = makeList(result.failure);

console.log(resultDisplayArray);
```

### Write Concise Object Literal Declarations Using Simple Fields:

```js
const createPerson = (name, age, gender) => {
  return {
    name: name,
	age: age,
	gender: gender
  };
};

console.log(createPerson("Ehsan Azari", 36, "male"));
```
-->
```js
const createPerson = (name, age, gender) => ({name: name, age: age, gender: gender});

console.log(createPerson("Ehsan Azari", 36, "male"));
```

### Write Concise Declarative Functions:

```js
const bicycle = {
  gear: 2,
  setGear(newGear) { // <-- setGear: function(newGear)
    "use strict";
	this.gear = newGear;
  }
};

bicycle.setGear(3);
console.log(bicycle.gear);
```

### Use Class Syntax to Define a Constructor Function:

```js
var SpaceShuttle = function(targetPlanet) {
  this.targetPlanet = targetPlanet;
};
var Zeus = new SpaceShuttle('Jupiter');

console.log(Zeus.targetPlanet);
```
-->
```js
class SpaceShuttle {
  constructor(targetPlanet) {
  this.targetPlanet = targetPlanet;
}
}
var Zeus = new SpaceShuttle('Jupiter');

console.log(Zeus.targetPlanet);
```
```js
function makeClass() {
  class vegetable {
    constructor(name) {
	  this.name = name;
	}
  }
  return vegetable;
}

const vegetable = makeClass();
const carrot = new vegetable('carrot');

console.log(carrot.name);
```

### Use gatters and setters to Control Accesss to an Object:

```js
class Book {
  constructor(author) {
    this._author = author;
  }
  
  // getter
  get writer() {
    return this._author;
  }
  
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
```	
```js
function makeClass() {
  class Thermostat {
    constructor(temp) {
	  this._temp = 5/9 * (temp - 32); // Fahrenheit to Celsius
	}
	
	get temperature() {
	  return this._temp;
	}
	
	set temperature(updatedTemperature) {
	  this._temp = updatedTemperature;
	}
  }
  
  return Thermostat;
}

const Thermostat = makeClass();
const thermos = new Thermostat(76);
let temp = thermos.temperature;
thermos.temperature = 26;
temp = thermos.temperature;

console.log(temp);
```

### Understanding the Differences Between `import` and `require`:

```js
/* to let it be exportable */

export const  capitalizeSrting = str => str.toUpperCase();

/* to import */

import {capitalizeSrting} from "./string_function" // from "./fileName" | if it's default it doesn't need {}
```

### Use `export` to Reuse a Code Block:

```js
export {function};
export const = ...;
```

### Use `*` to Import Everything from a File:

```js
import * as capitalizeSrting from "./string_function"
```

### Create an Export Fallback with export default:

```js
export default function subtract(x, y) {return x - y;}
```

### Import `export default`:

```js
import capitalizeSrting from "./string_function" // if it's default it doesn't need {}
```


