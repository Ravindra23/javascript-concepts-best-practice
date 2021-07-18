<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/javascript.png">
  <h1>javascript-questions-best-practice</h1>
</div>

<details><summary><b> Table of Content</b></summary>
<p>

- [Introduction to Sets In Javascript ](#Sets)
- [One line code snippet to solve the most occuring problems](#One-line-code-snippet-to-solve-daily-problems-on-array)

</p>
</details>


## Sets

### 1. Creating Sets
const mySet = new Set()

### 2. Adding values to set - "add()"
- mySet.add("I am a javascript set"); // string 
- mySet.add(3456);          // number 
- mySet.add(false);         // boolean 
- mySet.add({firstName:"set001"});         // object 
<p>console.log(mySet); <br>
<strong>Output:-  Set {"I am a javascript set", 3456, false, {firstName:"set001"}} </strong></p>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.add('🍍'); 
<p>console.log(fruitSet)<br> 
<strong>Output:-  Set {'🍌','🍇', '🍊', '🍎','🍍'} </strong></p>

### 3. Removing a value from set - "delete()"
- mySet.delete(3456)
<p>console.log(mySet); <br>
<strong>Output:-  Set {"I am a javascript set", false, {firstName:"set001"}} </strong></p>
- Other example:

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.delete( '🍎'); 
<p>console.log(fruitSet); <br>
<strong>Output:-  Set {'🍌','🍇', '🍊'} </strong></p>

### 4. Removing all values from set - "clear()"
- mySet.clear()
<p>console.log(mySet); <br>
<strong>Output:-  Set {} </strong></p>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.clear(); 
<p>console.log(fruitSet); <br>
<strong>Output:-  Set {} </strong></p>

### 5. Check existing value from set - "has()"
<p>console.log(mySet.has(false)); <br>
<strong>Output:-  true </strong></p>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
<p>console.log(fruitSet.has('🍍')) <br>
<strong>Output:-  false </strong></p>

### 6. Get size of a set - "size"
<p>console.log(mySet.size); <br>
<strong>Output:-  4 </strong></p>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎','🍍'); 
<p>console.log(fruitSet.size); <br>
<strong>Output:-  5 </strong></p>

### 7. Iterating over set with forEach()
- mySet.forEach(item=>{
    console.log(item);
})<br>
<p><strong>Output:-  "I am a javascript set", 3456, false, {firstName:"set001"}</strong></p>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- mySet.forEach(fruit=>{
    console.log(fruit);
})<br>
<p><strong>Output:-  '🍌','🍇', '🍊', '🍎' </strong></p>


## One-line-code-snippet-to-solve-daily-problems-on-array

### 1. If the conditional function is true/false for all elements- "isAll"
const isAll = (array,func) => array.every(func) ;

<strong>Examples</strong>
<ul>
<li>const result = isAll(['🍌','🍇', '🍊', '🍎'], (fruit)=> fruit === '🍍'));
<p>console.log(result); <br>
<strong>Output: false</strong></p></li>

<li>const result = isAll(['🍌','🍇', '🍊', '🍎'], (fruit)=> fruit === '🍊'));
<p>console.log(result); <br>
<strong>Output: false</strong></p></li>

<li>const result = isAll([1,2,3,4,5],(num)=> num< 10));
<p>console.log(result); <br>
<strong>Output: true</strong></p></li>

<li>const result = isAll([1,2,3,4,5],(num)=> num< 5));
<p>console.log(result); <br>
<strong>Output: false</strong></p></li>
</ul>

### 2. Return all indexes of element(value) in an array at once- "getIndexes"
const getIndexes = (array,value) => array.reduce((accumulator,element,index)=>(element===value ? [...accumulator,index]: accumulator),[]);

<strong>Examples</strong>
<ul>
<li>const result = getIndexes([1,2,1,4,5,1,3],1);
<p>console.log(result); <br>
<strong>Output: [0, 2, 5]</strong></p></li>

<li>const result = getIndexes(['🍌','🍎','🍇', '🍊', '🍎'],'🍎');
<p>console.log(result); <br>
<strong>Output: [1, 4]</strong></p></li>
</ul>
