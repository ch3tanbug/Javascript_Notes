# JavaScript Notes

A brief collection of curated notes created for those who want to learn JavaScript.

## Authors

- [@ch3tan_bug](https://www.linkedin.com/in/chetan-kashyap)

## Data-Types in JavaScript
### Primitive
1. N = NULL
2. N = NUMBER
3. S = STRING
4. S = SYMBOL
5. B = BOOLEAN
6. B = BIGint
7. U = UNDEFINED

- `var` declaration has global scope whereas `let` declaration has block scope

### Non-Primitive Data-Types

 OBJECT - Key:value pair 

- element can be accessed in two ways:
    1. `console.log(object["key"]);`
    2. `console.log(object.key);`

 `typeof()` - to know datatype of a variable

## Operators in JavaScript

### Arithmetic Operators
- `+` - add
- `-` - subtract
- `*` - multiply
- `/` - divide (always return concise value in decimal not like round off in C)
- `**` - power
- `%` - modulo (remainder)
- `++` - increment
    - `a++` = first print then increment
    - `++a` = first increment then print
- `--` - decrement
    - `a--` = first print then decrement
    - `--a` = first decrement then print

### Assignment Operators
- `=` - x=y
- `+=` - x=x+y
- `-=` - x=x-y
- `*=` - x=x*y
- `/=` - x=x/y
- `%=` - x=x%y
- `**=` - x=x**y

### Comparison Operators
- `==` - equal to
- `!=` - not equal
- `===` - equal value and type
- `!==` - not equal value or not equal type
- `>` - greater than
- `<` - less than
- `>=` - greater than or equal to
- `<=` - less than or equal to
- `?` - ternary operator

### Logical Operators
- `&&` - logical and
- `||` - logical or
- `!` - logical not 

### Comments - To ignore text in JavaScript
- `//` - single line Comments
- `/* "anything" "anything" */` - multiline Comments

### Conditional Expressions
1. `if` statement - `if() { 
any statements }`
3. `if-else` statement - `if() { any statement } else { any statement }`
4. `if-else-if-else` statement - `elseif() { any statement }`
5. `switch` statement -
```javascript 
switch(expression){
case 1 "anything":
code
break;
case 2 "anything":
code
break;
deafult:
code
}
```
5. Ternary operator - `console.log(age<18? "not drive" : "drive")` (shortcut for `if`)

#### Converting string to integer
```javascript 
let a = prompt("Enter your age"); // age entered here will always be of string type
a = Number.parseInt(a); // this will convert it to a number
```

# Loops & Functions

## Loops

1. For Loop-
```javascript
for(let i=0; i<10; i++){
console.log(i)
}
```

`Object.keys(objectname).length` - stores the length or number of keys in an object.

2. For in Loop - used to parse through the keys of an object.

Syntax:
```javascript
for(a in obj){
console.log(a) // will print all keys of the object obj
}
```


3. For of Loop - used to parse through the values of an object (also works in array).
```javascript
for(a in "chetan"){
console.log(a) // will print 'c' 'h' 'e' and so on
}
```


4. While Loop
```javascript
while(condition){
code to be executed
}
```


5. Do-while Loop - executes at least once.
```javascript
do{
commands to execute
}
while(condition)
```


### Functions

Syntax:
```javascript
function myfuncname(argument){
code to be executed
}
```


`const myfuncname=(arguments)=>{ code to execute }` - arrow functions.

`Object.keys(object name)` - used to extract keys and store in an array of an object.

`Object.keys(object name)[i]` - `i` is used to increment the keys and print desired key.

# CH-4 STRINGS

1. Strings are a collection of characters.
    - `stringVariable.length` // prints the length of the string
    - Strings can be written with both `""` and `''`.
    - `string[0-1--soo on]` // used to extract specific characters from string
2. Template Literals - backticks `` ` ``
   - `${var1} is a friend of ${var2}` // anything inside `${}` would be considered as a variable. No need to use `+` and `" "` again and again.
   - We can insert variables directly in template literal. This is called string interpolation.
3. We cannot print strings like `'MR's johnny'` because `'` is reserved.
   - We can use `\'` (escape character) - `'MR\'s jhonny'`
   - `\n` = new line
   - `\r` = carriage return
   - `\t` = tab
4. STRING Methods
   1. `length` - `string.length` // This is property so no need of `()`.
   2. `toUpperCase()` - `string.toUpperCase()` // This is function so need of `()`.
   3. `toLowerCase()` - `string.toLowerCase()`
   4. `slice()` - `string.slice(2,4)` // It will print 2nd and 3rd character. 4th not included.
   5. `replace()` - `string.replace("che","tan")`
   6. `concat()` - `string1.concat(string2,"anything")` // We can also use `+`.
   7. `trim()` - `string.trim()`  // Removes whitespaces "  ab" to "ab".
   8. `includes()` - `string.includes("anyword")` // If word is present returns true.
   9. `startsWith()` - `string.startsWith("word",position if req)` // If present, true.
   10. `endsWith()` - `string.endsWith("word",position if req)`

Strings are immutable.

# CH-5 ARRAYS

Arrays are variables which can hold more than one value. 

```javascript
let arryname=[1,2,3,4];
console.log(arryname);
console.log(arryname[index]);
```

`strorarry.length` returns the number of elements, not n-1.

### Adding New Elements To Array
```javascript
arrname[4]=5;  // adding
arryname[0]=9; // updating
```

Arrays are mutable but strings are not.

### Methods Of Array

   1. `toString()` - `arrname.toString()`
   2. `join()` - `arrname.join("-")` // join all elements with given character
   4. `pop()` - `arrname.pop()` // deletes last element from the original array and returns popped element
   5. `push()` - `arrname.push(element to add)` // adds a new element to the end of the array and returns the new array size
   6. `shift()` - `arrname.shift()` // removes the first element and returns it, modifies the original array
   7. `unshift()` - `arrname.unshift(element to add)` // adds an element to the start of the array and returns the new array length
   8. `delete` - `delete arrname(index)` // (this is a property) removes an element but that space remains empty, array length is not changed
   9. `concat()` - `arr1.concat(arr2, arr3, arr4)` // joins both arrays and can be stored in a new array
   10. `sort()` - `arr.sort()` // (modifies original array) sorts alphabetically
    
   create a compare function like -
   ```javascript
   const compare=(a,b)=>{
    return(a-b);
}
```

use this in sort - `arr.sort(compare)` // this will give sort in ascending order b-a will give in descending

10. `reverse()` - reverses the original array
11. `splice()` - `arr.splice`(startIndex, numberOfElementsToDelete, elements) // (returns deleted items and modifies array) arr.splice(2, 3, 4565, 76)
12. `slice()` - `arr.slice`(startIndex, endIndex) // excludes the endIndex element, creates a new array

### Looping in Arrays

1. `forEach()` -
```javascript
arrname.forEach((element)=>{
    // any commands
});
```

Syntax-
```javascript
arrname.forEach((value,index,array)=>{
    // any commands
});
```

2. `Array.from("chetan")` - used to create an array from an object // returns `['c','h','e']` and so on
3. `for in loop` - returns index (keys) of the array
4. `for of loop` - returns values (elements of array)
5. `map()` -
```javascript
arr.map((element)=>{
    // program logic (commands)  // same as forEach but performs actions and creates a new array
});
```

Syntax-
```javascript
map() - arr.map((value,index,array)=>{
    // program logic (commands)  // if you use all three arguments, the output will be like 47(value) 0(index) [47,0,1](arr)
});
```

6. `filter()`-
```javascript
arr.filter((element)=>{
    return element < 10;                 // filter values based on functions and returns in a new array
});
```

7. `reduce()` - reduces an array to a single value
  - eg- arr.reduce(add())   // `[1+2+5+6+7]` for array of `[1,2,5,6,7]` 

# JAVASCRIPT IN BROWSER

Browser has an embedded engine called the JAVASCRIPT engine

F12 - OPEN DEVTOOLS

Elements tab - open all elements of the page

Console Tab - all the errors + logs

Network Tab - all network requests

The `<script>` tag - use to add JAVASCRIPT in a HTML document

`<script>any js code</script>` or

`<script src ="https://jsfilesource">`

Benefits of using script tag using `src` attribute -

1. Separation of concerns
2. Browser caching

Console object methods -

- `console.log()` - prints msg in console
- `console.error()` - prints msg in console as error(red)
- `console.assert()` - shows assertion is true or not // console.assert(5>6)  which return assertion failed
- `console.clear()` - clears the console
- `console.table(objname)` - turns object into a table
- `console.warn()` - prints msg in console as warning(yellow)
- `console.info()` - same as console.log() just creates a info tab in console
- `console.time()` - starts the timer
- `cosole.timeEnd()` - stops the timer
- `alert()` - to invoke a mini-window
- `prompt()` - it can also be given a default value like `prompt("Enter",44)`
- `confirm()` - shows a message and waits for the user to press ok or cancel.
- `document.write("anything")` - adds to the webpage

### window object, BOM and DOM

1. `window` is a global object it has sub-objects like
   1. DOM(document object model) - simply an object of all the HTML
      `document.body.style.background="red"`  // changes colour of webpage
   2. BOM(browser object model) - to interact with other objects provided by the browser
      `alert()`, `confirm()`, `prompt()` are its part
      `location.href="google.com"` //redirects
   3. JAVASCRIPT core

# DOM

DOM tree refers to an HTML page where all the nodes are objects. 3 main types of nodes are:

1. Text nodes
2. Element nodes
3. Comment nodes

In an HTML page, `<html>` is the root, and `<head>` and `<body>` are its children.

4. Auto-correction - When we don't close tags properly in an HTML document or write some arbitrary HTML, the browser corrects it automatically.

`document.body` - returns the body of HTML.

`document.documentElement` - returns the page HTML.

`document.head` - returns the page head.

`document.title` - returns title (in string type).

If you access any element by `document` before actually declaring it, it will return null.

Directly as well as deeply nested elements of a document are called its children, like:

```html
<body>
  <div>hello</div> <!-- Here, div is a child -->
</body>
```

Child nodes - Elements that are direct children are called child nodes. E.g., `<head>` and `<body>` are of `<html>`.

Descendant nodes - all nested elements, their children, and children's children, and so on.

To access the first child of an element, last child, and all children:
```javascript
document.body.firstChild;
document.body.lastChild;
document.body.childNodes;
```

`element.haschildNodes` - to check whether the given element has any child nodes.

Child nodes look like an array but are not an array. We can use `Array.from()` to convert them into an array.

DOM collections:

   They are read-only.
   They are live - `element.childNodes()` will automatically update anything changed.
   They are iterable using for-loop.

Siblings are the nodes of the same parent. `body` is called the right or next sibling of `head`. `head` is called the previous or last sibling of `body`.
```javascript
element.nextSibling;
element.previousSibling;
```

We can access the parent of an element by using `element.parentNode` (print any nodes even if space, it prints text node) or `element.parentElement` (only valid HTML data).

Similarly, `element.firstElementChild`, `element.lastElementChild`, `element.previousElementSibling`, `element.nextElementSibling`.

Table-based navigation:
```javascript
table.rows // returns rows in HTML format
table.caption // reference to <caption>
table.tHead // reference to <thead>
table.tFoot // reference to <tfoot>
table.tBodies // reference to <body>
tBody.rows // rows inside any t body
tr.cells // collection of td and th
tr.SectionRowIndex // row number starting from 0
td.cells // no of cells inside enclosing <tr>
```

### Searching the DOM:

DOM navigation properties are helpful when elements are very close to each other:

   1. `document.getElementById("id here")`
   2. `document.querySelectorAll` - returns all elements inside an element matching CSS selector.
   3. `document.querySelector` - returns the first element (CSS)[0] of all elements inside an element matching CSS selector (same as `element.querySelectorAll(css)[0])`.
   4. `document.getElementsByTagName` - returns elements by given tag name.
   5. `document.getElementsByClassName` - returns elements by given class name.
   6. `document.getElementsByName` - searches for elements by the name attribute.
 
Matches,Closest & Contains
1. `element.matches(css)` - returns true if an element matches a CSS selector.
2. `element.closest(css)` - to look for the nearest ancestor that matches the CSS selector. First of all, the element itself is also checked.
3. `element.contains(element)` - returns true if element B is inside element A (a descendent of element A ) or if element A == element B.

# CH-8 Events and other DOM properties

- `console.dir()` shows an element as an object with its properties
- `element.tagName` returns tag name of an element
- `element.nodename` - exists for any node (comment,text)
- `innerHTML` property allows us to get HTML inside an element as a string (valid for element nodes only)
- `outerHTML` contains both the `innerHTML` and the element itself
- `element.textContent` provides all the text inside the element only text no tags
- `.hidden` specifies whether the element is visible or not
example-
```html
        <span id="hello" hidden> helloimspan </span>
```
```javascript 
document.getElementById("hello").hidden=false // will now show the content on the web page
```

- Attribute methods:
  1. `element.hasAttribute(name)` - method to check for existence of an attribute
  2. `element.getAttribute(name)` - method used to get the value of an attribute
  3. `element.setAttribute(name, value)` - method used to set value of an attribute
  4. `element.removeAttribute(name)` - method used to remove an attribute
  5. `element.attributes` - method used to get all the attributes of an element
  
- Insert Adjancent/HTML/Text Element
 1. `element.insertAdjacentHTML("beforeend", "<div id=second>second</div>")` -  insert before closing of element
 2. `element.insertAdjacentHTML("beforebegin", "<div id=second>second2</div>")` - insert before starting of element
 3. `element.insertAdjacentHTML("afterbegin", "<div id=second>second3</div>")` - insert just after element begin
 4. `element.insertAdjacentHTML("afterend", "<div id=second>second4</div>")` - insert after ending of element
 
- HTML insertion methods:
  - `nodeany.append(element)` - appends at the end of the node inside class
  - `nodeany.prepend(element)` - appends at the start of the node inside class
  - `nodeany.before(element)` - inserts before node outside class
  - `nodeany.after(element)` - inserts after node outside class
  - `element.insertAdjacentHTML(position, text)` - insert HTML at a specific position relative to the element
- Class name and class list:
  1. `element.classList.add/remove("classname")` - adds or removes a specific class
  2. `element.classList.toggle("classname")` - adds if class isn't present if present deletes it
  3. `element.classList.contains("classname")` - checks for a given class returns true/false
  4. `element.className = "red"` - overwrites existing class
- `setTimeout(function(), delay, argument1, argument2)` - allows us to run a function once after an interval of time
example-
```javascript
            example-
            setTimeout(function(){
                alert(2)  // here 2000 means 2000ms (once)
            },2000) 
  ```
- `clearTimeout(intervalID)` - used to cancel the execution of `setTimeout`
- `setTimeInterval(function(), delay, argument1, argument2)` - to run function indefinitely after an interval of time
example-
```javascript
        setTimeInterval(function(),delay,argument1,argument2) - to run function indfinitely after interval of time
            setTimeInterval(function(){
                alert(2)  // runs after 5 secs
            },5000)
 ```
- `clearInterval(intervalID)` - used to cancel the execution of `setInterval`
- Introduction to browser events:
  - An event is a signal that something has happened all DOM nodes generate a signal
  - Some important DOM events: 
    1. Mouse event - click, contextmenu (right-click), mouseover/mouseout, mousedown/mouseup, mousemove
    2. Keyboard events - keydown and keyup
    3. Form element event - submit, focus, etc.
    4. Document events - DOMContentLoaded
- Handinling events:
  - Events can be handled through HTML attributes
  ```html
    <input value="hey" onclick="alert('hey')" type="button">```

 - Events can also be handled in JavaScript by `.onclick` property
  ```javascript
              document.getElementsByTagName("div")[0].onclick=function(){
                alert(1) // using like this in js will override the previous handler
            }
  ```
- `addEventListener` and `removeEventListener` are used to assign and remove handlers to an event
   ```javascript
                element.addEventListener(event,handler)
                element.removeEventListener(event,handler) // handler must be same function object to work

            example -
                let x = function() {
                alert("hello world1")
                }

                btn.addEventListener('click', x)
                let y = function() {
                alert("hello world2")
                }
   ```

- The Event object:
  - When an event happens, the browser creates an event object, puts information about the event into it, and passes it as an argument to the handler function
```javascript
            element.onclick=function(event){
                    console.log(event)
            }
            event.type - event type
            event.currentTarget - element that handeled the event
            event.clientX/event.clientY - 
            

                btn.addEventListener('click', y)

                let a = prompt("what is your favourite number")

                if (a == 2) {
                btn.removeEventListener('click', x)
                }
  ```

element.closest(css) - to look for the nearest ancestor that matches the CSS selector. First of all, the element itself is also checked.

# Callbacks Promises async/await
Asynchronus actions are the actions that we initiate now and they finish later. eg -setTimeOut 

Asynchronus actions are the actions that initiate and finish one by one

### Callback function
A Callback function is a function that is passes as an argument into another function, which is then invoked inside the outer function to complete a action

example -
```javascript
            function loadscript(src, callback) {
            let script = document.createElement("script")
            script.src = src
            script.onload = function() {
                console.log("src: " + src)
                callback(src)
            }
            document.body.appendChild(script)

            }
            const hello = (src) => {
            alert("hello" + src)
            }
            loadscript("https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js", hello)
```    

This is called call-based style of asynchronus programming. a function that does something asynchronously should provide a callback argument where we put function to run after its complete

- Error Handling -

example -
```javascript
    function loadscript(src, callback) {
    let script = document.createElement("script")
    script.src = src
    script.onload = function() {
    console.log("src: " + src)
    callback(null, src)
    }
    script.onerror = function() {
    let error = "this is an error"
    callback(error, src)
    }
    document.body.appendChild(script)

    }
     const hello = (error, src) => {
    if (error) {
    console.log("got error")
    return
    }
    alert("hello" + src)
    }
    loadscript("https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js", hello)
```

### Callback Hell / Pyramid of DOOM (solution-promises)
When we have callbacks inside of callbacks the code gets difficult to manage as calls become more nested the code become deeper and and increasingly more difficult to manage this is called Pyramid of dom, the pyramid of these calls grows towards right with every asynchronus action.
soon it spitals out of control this way of coding isnt very good.
        
### Promises
The olution to callback hell is promises. Promise is a "promise of code execution", the code either executes or fails in both the cases the user will be notified

Syntax-
```javascript
                let promise=new Promise(function(resolve,reject){
                    any code
                    resolve()
                    reject()
                })
 ```
resolve(value) - if the job is finished successfully

reject(error) - if the job fails

The promise object returned by the new promise constructor has these three properties-
            1. state: initially pending, then changes to fulfill if resolved() is called or rejected when
            reject() is called.
            2. result: initially undefined then changes to value if resolved() is called or error if reject() is called

### Consumers: .then&.catch
The consuming code can retrieve the result of the promise using through then and catch
```javascript
                promise.then(function(result){
                    handle here through code
                },function(error){
                    handle error here through code 
                })
```

if we are interested only in successfully completng the program we can only use .then with one argument

if we are inetrested in catching errors we can either use 
```javascript
.then(null,function(error){
 here code
 }) or the .catch method
```

### Promise Chaining
We can chain promises and make them pass resolved values to one another
```javascript
        
            p1 = new Promise((resolve, reject) => {
            setTimeout(function() {
                console.log("resolved after 2 seconds")
                resolve(56)
            }, 2000)
            })
            p1.then(function(value) {
            console.log(value)
            let p2=new Promise((resolve,reject)=>{
                setTimeout(()=>{
                resolve("promise 2")
                },2000)
            })
            return p2
            }).then((value) => {
            console.log("we are done")
            })
```

### Attaching multiple handlers
We can attach multiple handlers to a single promise they do not pass the value to each other rather they process it independently.

if p is a promise then-
  `p.then((handler1))`
        
  `p.then((handler2))` // Attaching multiple handlers
       
  `p.then((handler3))`

### The Promise API 
There are 6 static methods of promise class-
1. `Promise.all([promises])` - waits for all promises to resolve and returns the array of these results  if any one fails it becomes the error and all others passed are ignored.
2. `Promise.allSelected([promises])` - waits for all the promises to settle and returns this result as an array of objectswith status and value
3. `Promise.race([promises])` - waits for the first promise to settle and its result/error becomes the outcome.
4. `Promise.any([promises])` - waits for the first promise to fulfill (not rejected) and its result becomes the outcome if 1st promise is rejected it gives output of next promise which is fulfilled and if all promises are rejected it throws a Aggregate Error
5. `Promise.resolve(value)` - makes a resolved promise with given value
6. `Promise.reject(error)` - makes a rejected promise with given error

### ASYNC/AWAIT 
There is a special syntax to work with promises in JAVASCRIPT a function can be made async by using async keyword like this - 
```javascript
            async function chetan(){
                return(7)
            }
```
An async function always returns a promise other values are wrapped in a promise automatically await is used inside async function and awaits for the process to finish before executing next line

Example -
```javascript
                async function chetan() {
                    let delhiweather = new Promise((resolve, reject) => {
                        setTimeout(() => {
                        resolve("22 degree")
                        }, 1000)
                    })

                    let bangaloreweather = new Promise((resolve, reject) => {
                        setTimeout(() => {
                        resolve("27 degree")
                        }, 2000)
                    })
                    let delhim = await delhiweather
                    let bangm = await bangaloreweather
                    return [delhim, bangm]
                    }
```

### Error Handling(try/catch)
The try catch syntax allows us tomcatch errors so that the script instead of dying can do something moreresonable. try catch works synchronusly if an exception happens in a scheduled code like in set time out then try/catch wouldn't work

```javascript
                try{
                    console.log(rahul)
                }                                // will work
                catch(error){
                    console.log(error)
                }

                try{
                    setTmeout(()=>{
                        error code              // wont work
                    })
                }
                catch{

                }
```

### The error object 
For all the built in errors the error object has two main properties
```javascript
                try {
                    harry
                 }
                catch (error) {
                    console.log(error.name) // returns error name only
                    console.log(error.message) // returns only message thrown by error
                    console.log(error.stack) // returns error stack (type,name,location)
                }
```

### Throwing custom errors
We can throw our own error by using throw syntax
```javascript
                if(age<180){
                    throw new Error("invalid age")
                }
```

We can also throw other errors by using the built in constructor for standard errors    

`new SyntaxError(message)`

`new ReferenceError(message)`

### Finally Clause
The try:catch construct may have one or more code clause: finally
If it exists it runs in all cases:
1. After try if there were no errors 
2. After catch if there were errors

If there is a return in try finally is run just before the control is transferred to outer code.
- syntax:
 ```javascript
                try{

                }
                catch(error){

                }
                finally{

                }
```        
### The Fecth API
JAVASCRIPT can be used to send and retrieve information from the network when needed(AJAX). Fetch is used to get data over the internet

            `let promise=fetch(url,[options]) // without and options reuest type is get`
        
Getting a response is a two stage process-
1. an object of response class containing "status"&"ok" properties
- status- the http status code
- ok- boolean true if the http status code is between 200-299
2. after that we need to call a different method to access the body in different formats
- response.text() - read and returns the text
- response.json() - parse the response as json
Others method include response.formData() response.blob() response.arrayBuffer()

Note - we can only use one body reading method at a time if we have already got the text with response.text() then resonse.json() won't work

### Response headers-
Response headers are available in response.headers

### Request Headers-
To set a reuest header in fetch , we can use the header option 
```javascript
        response=fetch(url,{
            header:{
                authentication:"secret"
            }
        })
```       

To make a post request we need to use the fetch options

Example-
```javascript
            const createtodo = async (todo) => {
            let options = {
                method: "POST",
                headers: {
                "Content-type": "application/json"
                },
                body: JSON.stringify(todo)

            }


            let p = await fetch('https://jsonplaceholder.typicode.com/posts', options)
            let response = await p.json()
            return response
            }

            const getid = async (id) => {
            let p = await fetch('https://jsonplaceholder.typicode.com/posts/' + id)
            let r = await p.json()
            return r

            }

            const mainfunc = async () => {
            let todo = {
                title: 'foo',
                body: 'bar',
                userId: 1,
            }
            todor = await createtodo(todo)
            console.log(todor)
            console.log(await getid(5))
            }
            mainfunc()
```

### Cookies in JAVASCRIPT
Cookies are small strings of data directly stored in the browser in JAVASCRIPT document.cookie provides access to the browser Cookies

### Writing to cookie
An assignment to document.cookie is totally specifically in a way that a write operation doesnt touch other code to update (append a cookie):
            `document.cookie="chetan=100" // cookies are always written in key=value pair`
    
`encodeURIComponent`

This helps keep valid formatting by encoding any special characters

Syntax- 
            `${encodeURIComponent(key)}=${encodeURIComponent(value)}`

`decodeURIComponent` this helps to decode any url encoding `decodeURIComponent("%27%18")`
    
### Cookie options  
Cookies have several options which can be provided after key=value to a set call like this

`document.cookie="user=john;path=/a;expires=Tue,29th march`

 Path makes cookie available at /a,/a/,a/any etc and expires tells the cookie expiration time
 
 Note:
 1. The name=value in cookie should not exceed 4kb
 2. Total number of cookies in browser is limited to 20+(generally depends on the browser)

