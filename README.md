<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/javascript.png">
  <h1>javascript-questions-best-practice</h1>
</div>

<details><summary><b> Table of Content</b></summary>
<p>

- [Introduction to Sets In Javascript ](#Sets)

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
#### console.log(mySet);   
#### Output:-  Set {"I am a javascript set", 3456, false, {firstName:"set001"}}
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.add('🍍'); 

#### console.log(fruitSet);  
#### Output:-  Set {'🍌','🍇', '🍊', '🍎','🍍'} 

### 3. Removing a value from set - "delete()"
- mySet.delete(3456)
#### console.log(mySet) ;  
#### Output:-  Set {"I am a javascript set", false, {firstName:"set001"}}
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.delete( '🍎'); 

#### console.log(fruitSet);   
#### Output:-  Set {'🍌','🍇', '🍊'} 

### 4. Removing all values from set - "clear()"
- mySet.clear()
#### console.log(mySet);   
#### Output:-  Set {}
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.clear( '🍎'); 

#### console.log(fruitSet);  
#### Output:-  Set {} 

### 5. Check existing value from set - "has()"
- mySet.has(false)
#### console.log(mySet);   
#### Output:-  true
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- fruitSet.has('🍍'); 

#### console.log(fruitSet);   
#### Output:-  false 

### 6. Get size of a set - "size"
#### console.log(mySet.size);   
#### Output:-  4
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎','🍍'); 

#### console.log(fruitSet.size);   
#### Output:-  5 

### 7. Iterating over set with forEach()
- mySet.forEach(item=>{
    console.log(item);
})
#### Output:-  "I am a javascript set", 3456, false, {firstName:"set001"}
<br>
- Other example: 

- const fruitSet = new Set('🍌','🍇', '🍊', '🍎'); 
- mySet.forEach(fruit=>{
    console.log(fruit);
})
#### Output:-  '🍌','🍇', '🍊', '🍎' 


