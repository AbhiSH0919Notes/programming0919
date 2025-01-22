
>[!SUMMARY]- JavaScript
 >  1) JavaScript was invented by **Brendan Eich** in **1995**.
 >  2) And later it became an **ECMA Standard** in **1997.**
 >  3) JavaScript was *developed to add interactivity (such as animation & hover) on web pages*.
 >  4) It is **high-level, object oriented** programming language.
 >  5) It is mainly Invented for **client side** (front end) programming on web.
 >  6) It is **case sensitive** programming language.
 >  7) The **version from ES6(2015)** and onwards is known as **Modern JavaScript**.
 >  8) **All browsers come** with the **JavaScript Engine**. (Interpreted by all modern-day browsers)


>[!NOTE]- JavaScript Functions
>- Three different ways of writing javaScript functions, but they all work in a similar way.
>- **Receive input data ---> Transform data ---> Output data**
>
>	**1) Function Declaration : We can use function before its declared. (hoisted)**
> 		  - `function funName(parameter) {`
> 			`return parameter;`
> 		 `}`
> 		 `funName(argument);`
> 		 
>	**2) Function Expression : We can use store function in variable & we cant call before its declared.**
> 		-	`const funName = function (parameter) {`
> 			`return parameter;`
> 		 `}`
> 		 `const data = funName(argument)`
> 		 
> 	**3) Function Arrow : One line & automatically return value.**
> 		- `const funName = (parameter) => parameter;`
> 		




#### 1) ways to print in JavaScript
 ```js
alert("Hello World !");
 console.log("hello abhi");
 document.write('this is document.write for print on screen')
```

#### 2) JavaScript console API (Application Programming Interface)
```js
 console.log("hello world", 9 + 9);
 console.warn("this is an warning.");
 console.error("this is an error.");
```

#### 3) Variables in JavaScript - Containers to store a data value
  ```js
var variable = dataType; // var is a function scope variable.
let variable = dataType; // let is a block scope variable & we can mutate this variable.
const variable = dataType; // const is also block scope variable but we cant mutate this variable.
```


#### 4) there are main two categories of data types in JavaScript:
  ##### **1) Primitive data type** : 1} Null 2} Undefined 3} Number 4} String 5} Booleans 6} Symbol 7} BigInt
  ##### **2) Reference data type** : 1} Objects 2} Arrays
```js
// 1) Primitive data types in JavaScript

  // null (empty data type)
	  let empty = null;

  // undefined (not define any value/data)
	  let abhishek;

  // numbers
	  let num1 = 19;
	  let num2 = 32;

  // strings (sentence)
	  let str1 = "this is a string";
	  let str2 = "this is also string";

  // booleans (true or false)
	  let abhi = true;
	  let shek = false;

// 2) Reference data types in JavaScript
  // objects (tables/sheets)
	   let marks = {
	      abhi: 80,
	      sonu: 80,
	      ganesh: 80
	   };
```


#### 5) Operators in JavaScript
 ***1) Arithmetic Operators*** : [ +, -, *, /, ** ]
 ***2) Assignment Operators*** : [ = ]
 ***3) Comparison Operators*** : [ <, >, <=, >= ]
 ***4) Logical Operators*** : [ &&, ||, ! ]

 ```js
// 1) Arithmetic operators [calculation between variables]
 var a = 100;
 var b = 10;
 console.log("the value of a + b is ===> 100 + 10", a + b);
 console.log("the value of ++a is ===> a + 1", ++a);
 console.log("the value of --a is ===> a - 1", --a);
 console.log("the value of a ** n is ===> a^b", a ** b;
	 // operators and operand
	 // { a + b } --->[ (+) is operators ] and [ (a and b) is operand ]

// 2) Assignment operators [Assignning the value of variable]
 var c = b;
 c = c + 2;
 console.log("the value of c = b & c + 2 is", c);

// 3) Comparision operators [Compare between two values]
 console.log("the value of a, b is", a, b);
 console.log("the value of a >= b is", a >= b);
 console.log("the value of a <= b is", a <= b);
 console.log("the value of a > b is", a > b);
 console.log("the value of a < b is", a < b);

// 4) Logical operators [Logic between boolean values]
	// logical (and [ && ]) operator
	// If all values are true then output is true.
	// If any one value is false then output is false.
	console.log("the value of true && true is", true && true);
	console.log("the value of true && false is", true && false);
	console.log("the value of false && true is", false && true);
	console.log("the value of false && false is", false && false);

	// logical (or [ || ]) operator
	// If any one value is true then output is true.
	console.log"the value of true || true is", true || true);
	console.log"the value of true || false is", true || false);
	console.log"the value of false || true is", false || true);
	console.log"the value of false || false is", false || false);

	// logical (not [ ! ]) operators
	// When value is true then output is false & value is false then output is true.
	console.log("the value of !true is", !true);
	console.log("the value of !false is", !false);
``` 


#### 6) Types of Functions In JavaScript
```js
// 1) Arrow Function
		let avg = (a, b) => {
		   c = (a + b) / 2;
		  return c;
		}

// 2) Function Expression
		let avg = function(a, b) { 
		   c = (a + b) / 2;
		  return c;
		 }

// 3) Function Declaration
		function avg(a, b) {
		  c = (a + b) / 2;
		  return c;
		}

// Calling function with arguments
const abhi = avg(80, 20);
const sonu = avg(50, 30);
console.log(abhi, sonu);
```


#### 7) Conditions in JavaScript
 ```js
let age = 22;
// 1) Single if statement=
		if (age > 19) {
		    console.log("you are boy");
		}

// 2) if - else statement=
		if (age > 18) {
		    console.log("you are 18+ boy");
		} else {
		    console.log("you are kid");
		}

// 3) if - else ladder=
		if (age > 65) {
		    console.log("you are a old man");
		} else if (age > 30) {
		    console.log("you are a man");
		} else {
		    console.log("you are a boy");
		}
```


#### 8) Loops in JavaScript 
```js
// for-loop
		const arr = [1, 2, 3, 4, 5, 6, 7];
		
		for (var i = 0; i < arr.length; i++) {
		    // break and continue conditions
		    if (i = 2) {
		      //break; // after 2 number arrays will not displaying
		      continue; // display all numbers without 2 number
		  }
		    console.log(arr[i]);
		}

// forEach-loop
		arr.forEach(function (element) {
		    console.log(element);
		});

// while-loop
		let j = 0;
		while (j < arr.length) {
		
		  console.log(arr[j]);
		    j++;                             
		}

// do-while-loop
		do {
		    console.log(arr[j]);
		    j++;
		} while (j < arr.length);
```


#### 9) Array methods
```js
let myArr = ["car", "bike", "cycle", 9, "scooty", null, true, "abhi"];
	myArr.unshift("ABHISH");  // add string inside the array at the start
	myArr.shift();           // remove first string inside the array
	myArr.push("abhish");   // add string inside the array at the end
	myArr.pop();           // remove last string inside the array
	myArr.toString();     // convert array into string
	myArr.sort();        // sorting Alphabetically
	myArr.splice();     // remove one item
	myArr.slice();     // remove items or cut string
	myArr.length;     // count the array lenght
```


#### 10) String methods
```js
let myString = "this is a string methods in javascript";
	console.log(myString);
	console.log(myString.length); // counting length
	console.log(myString.indexOf("javascript")); // charactor or word find
	console.log(myString.lastIndexOf("t")); // last index charactor find
	console.log(myString.slice(1, 7)); // slicing in string / only show charactors between the number
	console.log(myString.replace("string", "string-replace")); // replace any word in string using replace
```


#### 11) Date Object and methods
```js
let myDate = new Date();
	console.log(myDate);
	console.log(myDate.getDate());
	console.log(myDate.getFullYear());
	console.log(myDate.getTime());
	console.log(myDate.getTimezoneOffset());
	console.log(myDate.getUTCDate());
```


#### 12) DOM (Document Object Modal)
 ```js
// Selecting dom element & style
	let firstId = (document.getElementById("firstContainer").style.background ="red");
	
	let firstTag = (document.getElementsByTagName("body")[0].style.background ="red");
	
	let firstClass = (document.getElementsByClassName("container")[1].style.background = "green");
	
	let firstquery = (document.querySelectorAll(".container")[2].style.background = "black");

		firstClass[1].classList.add("bg-primary");
		firstClass[1].classList.remove("bg-primary");

	let createOne = document.createElement("h2");
	let createTwo = document.createElement("h3");

		document.getElementsByTagName("div")[0].appendChild(createTwo);
		document.getElementsByTagName("div")[0].replaceChild(createTwo, createOne);
		document.getElementsByTagName("div")[0].removeChild(createOne);
```

#### 13) Set time out and set intervals
```js
	let login = () => {
	  document.querySelectorAll(".container")[1].innerHTML = "<b>we are fired</b>";
	  console.log("set time out or set interval");
	};

	const clrTimeout = setTimeout(login, 5000);
	const clrInterval = setInterval(login, 5000);
	
	clearTimeout(clrTimeout);
	clearInterval(clrInterval);
```


#### 15) Type Conversion & Coercion

> [!NOTE]- Conversion & Coercion
> 
> 	1) Conversion - We need to manually convert data types.
> 	2) Coercion - Convert data types automatically.

```Js
"9" - "5" = 4
"19" - "13" + "17" = "617"
"19" - "13" + 17 = 23
"123" < 57 = false
5 + 6 + "4" + 9 - 4 - 2 = 1143
```


#### 15) Small Utility
```js
// Confirm
	if (confirm("want to go google.com")) document.location.pathname = "google.com";

// Generate Random Number
	let randomNumber;
		randomNumber = Math.random() * 9; // set the maximum number
		randomNumber = Math.floor(randomNumber) * 9; // remove decimals
		console.log(randomNumber);

// Converting Object in JSON format
	let obj = { name: "abhi", fev: "game", num: 9, a: { this: "that" } };
	let jso = JSON.stringify(obj);
		console.log(obj);
		console.log(jso);

// Converting JSON to Object
	let parsed_jso = JSON.parse(jso);
	let parsed = JSON.parse(`{"name":"abhi","fev":"game","num":9,"a":{"this":"that"}}`);
		console.log(parsed_jso);
		console.log(parsed);
// Screen height
	const height = element.getBoundingClientRect().top/bottom/left/right;

// Mouse Click Event
	e.clientX // ===> clicked position left width
	e.clientY // ===> cliced position top height
	e.target.offsetLeft/Top/Right/Bottom // ===> getting offset from clicked position

// Locale Storage
	localStorage.setItem("Key", JSON.stringify(arrayName)); // ===> save data in local Storage
	JSON.parse(localStorage.getItem("Key")); // ===> get data from local Storage

// Other Operators
	? : true ? true : false // ===> Optional Chaining/Ternary Operator
	% : 3 % 2 = 1, 11 % 3 = 2, 19 % 4 = 3  // ===> Modual/Reminder Operator
	?? : 0 ?? 1 // ===> Nullish Coalescing Operator
	... : let a = ...[1,2,3] // ===> Spread Operator 1, 2, 3;
	... : let ...a = 1, 2, 3; // === Rest Operator [1, 2, 3];
```
