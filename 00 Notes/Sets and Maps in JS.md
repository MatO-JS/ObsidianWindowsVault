
source : chatGpt

### Sets in JavaScript

A Set is a collection of unique values where each value can occur only once. It can hold any type of values, whether primitive values or object references.

**Creating a Set:**

javascript

```javascript
// Creating a new Set
let mySet = new Set(); 
// Adding elements to the Set
mySet.add(1); mySet.add('hello'); mySet.add({ name: 'John', age: 30 }); 
console.log(mySet); // Set(3) { 1, 'hello', { name: 'John', age: 30 } }`

```
**Common Methods for Sets:**

- **`add(value)`**: Adds a new element to the Set. If the value already exists, it won't be added again.
- **`delete(value)`**: Removes a specific value from the Set.
- **`has(value)`**: Checks whether a value exists in the Set.
- **`clear()`**: Removes all elements from the Set.
- **`size`**: Property that returns the number of elements in the Set.

**Example:**

```javascript
let mySet = new Set(); 
mySet.add(1);
mySet.add(2);
mySet.add(3);
console.log(mySet.size); 

mySet.add(2); // Adding duplicate value

console.log(mySet.size); // Still Output: 3, because duplicates are not allowed

console.log(mySet.has(2)); // Output: true

mySet.delete(2);
console.log(mySet.has(2)); // Output: false

mySet.clear();
console.log(mySet.size); 

```



### Maps in JavaScript

A Map is a collection of key-value pairs where each key can be of any type and each key-value pair is unique.

**Creating a Map:**

javascript

`// Creating a new Map let myMap = new Map();  // Adding key-value pairs to the Map myMap.set('name', 'Alice'); myMap.set(1, 'One'); myMap.set({ id: 1 }, { name: 'Bob' });  console.log(myMap); // Map(3) { 'name' => 'Alice', 1 => 'One', { id: 1 } => { name: 'Bob' } }`

**Common Methods for Maps:**

- **`set(key, value)`**: Adds a new key-value pair to the Map. If the key already exists, it updates the corresponding value.
- **`get(key)`**: Retrieves the value associated with the specified key.
- **`has(key)`**: Checks whether a key exists in the Map.
- **`delete(key)`**: Removes a specific key-value pair from the Map.
- **`clear()`**: Removes all key-value pairs from the Map.
- **`size`**: Property that returns the number of key-value pairs in the Map.

**Example:**

javascript

`let myMap = new Map();  myMap.set('name', 'Alice'); myMap.set(1, 'One'); myMap.set({ id: 1 }, { name: 'Bob' });  console.log(myMap.get('name')); // Output: 'Alice'  console.log(myMap.has(1)); // Output: true  myMap.delete('name'); console.log(myMap.has('name')); // Output: false  console.log(myMap.size); // Output: 2  myMap.clear(); console.log(myMap.size); // Output: 0`

### Iterating over Sets and Maps

You can iterate over the elements of a Set using `forEach()` or using a `for...of` loop. Similarly, you can iterate over the entries of a Map using `forEach()` or using a `for...of` loop with destructuring.

**Iterating over a Set:**

javascript

`let mySet = new Set([1, 2, 3]);  // Using forEach mySet.forEach(value => console.log(value));  // Using for...of loop for (let value of mySet) {     console.log(value); }`

**Iterating over a Map:**

javascript

`let myMap = new Map([     ['name', 'Alice'],     [1, 'One'],     [{ id: 1 }, { name: 'Bob' }] ]);  // Using forEach myMap.forEach((value, key) => console.log(key, value));  // Using for...of loop with destructuring for (let [key, value] of myMap) {     console.log(key, value); }`

Sets and Maps in JavaScript are powerful data structures that provide efficient ways to manage collections of unique values (Sets) and key-value pairs (Maps). They are commonly used in various scenarios where you need to handle data with specific requirements such as uniqueness or key-based retrieval.