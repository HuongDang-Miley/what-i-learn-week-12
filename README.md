# Monday
## document.querySelector(str) 
A JS method to target HTML element and over write its CSS style </br>
Return an object which is the element being selected</br>
If there are many similar element (eg: li) only the first one will be return</br>
~~~
<h1>Hello World</h1>
const heading1 = document.querySelector('h1')
~~~
hold cmd + L / cmd + O : live server: to view on browser </br>
Opt + cmd + J: inspect on broswer </br>

# Tuesday
## addEventListener(event, func)
A type of call back function </br>
Take in an event ('click', 'mouseover',etc) then run a function that do something
~~~
const makeH1Blue = function() {
heading1.style.color = 'blue'
}
heading1.addEventListener('click', makeH1Blue)
~~~
## document.querySelectAll(str)
Select all similar element</br>
Return a NodeListOf element </br>.
Node list of has property like: length; forEach, Key, etch
~~~
<ul>
<li>Apple</li>
<li>Banana</li>
<li>Mango</li>
</ul>
const list = document.querySelectAll('li') // -> list is node list of <li>
~~~
To use .map() and .filter(), must convert the note list to an actual array

~~~
const listArray = Array.from(list) //-> listArray is an array of <li>
~~~~

## event property
Browser has its own property when mouse do something to an element, we can see it by running below function and check inspect page
~~~
const isClicked = function(event) {
console.log(event)
}
list.addEventListner('click',isClicked)
~~~
# Thursday
## .classList (prefer way because all method will be updated in the DOM)
Show classes of elements in form of object
## .className (not prefer because the DOM will not be manupulated)
Show classes of elements in form of strings. Therefore can be convert to array using .split(' ')
## .add('newClassName')
Add new class to an element
## .remove('className')
Remove a class from an element
## .contains('className')
check if an element has a class
~~~~
console.log(list1.contains('green')) //=> true
~~~~
## .toggle('className')
toggle on or off a class
~~~~
const toggleDarkMode = function () {
  list1.toggle('dark-mode')
}
~~~~

## .replace('className')
Replace a current class by another class 
~~~
list1.replace('high-contrast', 'low-contrast')
