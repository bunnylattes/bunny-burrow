---
class: webd 2008
module:  module five
date:  2022-03-06
tags: #webd-2008 #javascript #react #web-development 
---

# Javascript Review

## Javascript Advanced Topics

#### Debugging Javascript
- Inspect -> Console -> type out the code in the console
- Read Evaluate Print Loop: Type in code and it will immediately take effect.

#### Callback and Anonymous Functions

**setTimeout(snail, 2000);**
- first parameter is the function you call and the second is the number of milliseconds it will wait to execute the function
- no brackets when you pass a function!

**Attach a Function to a Variable** aka **A named, anonymous function**
- let snail = function() {
		console.log("Hello sail!")}

**Combination!**
- setTimeout(**function()** {*console.log("Hello World!");*} 1500);
- functions can be passed around a lot differently
- whatever goes in the first argument of setTimeout must be a function, the second must be a number.
- when executing in code, it's a function that isn't going to be reused (onclick or something like this)
- cleaner code!

#### Objects
- myObject = { myfnc: function() { console.log("Hello JS Object Function!"); }};
	- myObject.myfnc(); (key:value pairs)
	- this will print "Hello JS Object Function" in the console
	- this is the "old school way" of creating an object

#### Arrow Functions

**Using the Fat Arrow**
- let fail = function() {console.log("Hello Fail")}
- fail(); prints Hello Fail!
- let gail = () => { console.log("Hello Gail")}
- execute with **gail()** 
- Syntactic sugar: makes the language just a little sweeter to look at
- ***Removes the keyword function, sometimes called a fat arrow, -> are skinny or stabby arrows***

**Explicit Return Function**
- ```let explicit = (word, emoji) => {
	return `Hello ${word}! ${emoji}`;
   }```
- console.log(explicit('Rail' ,'🚆'));
- this will print "Hello Rail!  🚆"
- Backticks combined with ${keyword} are the special quotes for template string interpolation which removes the need for string concatenation (firstName + '  ' + lastName)
- ``` `${firstName} ${lastName}` ```

**Implicit Return Function**
- Removes start/stop braces { }
- Removes the keyword: return
- for SINGLE LINE return functions only!!
- ``` let implicit = (word, emoji) => `Hello ${word}! ${emoji}`; ```
- console.log(implicit('Rail', '🚆'));
- this will print "Hello Rail!  🚆"

**Unadorned Functions**
- Removes the parentheses for SINGLE PARAMETER functions only
- ``` let unadorned = emoji => `Hello Scale! ${emoji}`; ```
- console.log(unadorned('⚖'));
- this will print "Hello Scale! ⚖"

#### Javascript Looping

**Classic For Loop**
- ``` let fruitBasket = ['cherry', 'grape', 'watermelon', 'kiwi'] ```
- ``` for(let i = 0; i < fruitBasket.length; i++){
	console.log(fruitBasket[i]);
	} ```
- this will print off the array index

**For Loop with OF**
- ``` for(const fruit of fruitBackset){
	console.log(fruit);
	} ```
- this will print the same result as previous for loop, the variable ***fruit*** becomes the iteration of the loop instead of ***fruitBasket[i]***
- **const** is used here because there's no reason why fruit should ever be changed, it will be constant and read only

**For Each Loop**
- ForEach is a call back based loop
- this is a single line unadorned arrow function with 1 parametre
- ``` fruitBasket.forEach(fruit => console.log(fruit)); ```
- ***fruitBasket*** is the array, the variable is being assigned as ***fruit*** by the fat arrow
- printout will be identical to the last loops

**More Complex For Each Loop**
- we could use forEach to get the index value out
- ``` fruitBasket.fortEach( (fruit, i) => {
		let length = fruitBasket.length;
		let row = ' ' .repeat(length-i) + fruit.repeat(i+1);
		console.log(row)
	}); ```
- ***fruit*** will be the variable assigned, ***i*** will take the index
- in this printout, the spaces will decrease and the fruit will repeat based on how many iterations we have gone through

#### Array Helpers

``` 
const animals = [
		{ name: 'Monkey',  emoji: emj,  legs: 2, mana: 45,   count: 3},
		{ name: 'Dog',     emoji: emj,  legs: 4, mana: 89,   count: 2},
		{ name: 'Cow',     emoji: emj,  legs: 4, mana: 56,   count: 5},
		{ name: 'Dragon',  emoji: emj,  legs: 4, mana: 9001, count: 1},
		{ name: 'Deer',    emoji: emj,  legs: 4, mana: 98,   count: 18},
		{ name: 'Kangaroo',emoji: emj,  legs: 2, mana: 49,   count: 6},
		{ name: 'Turkey',  emoji: emj,  legs: 2, mana: 17,   count: 7},
	];
```
- a Javascript array of animals, each animal has a key value pairing (name, legs, mana, count = property names or keys)
- ``` animals[3] ``` will give the dragon object
- ``` animals[3].name ``` will give the name of the index: **Dragon**

**MAP**
- takes in a collection and makes a new collection of the same size, but modified in some way
- example: map the animals to a new array with a number of emojis equal to the count
	- ``` const emojiZoo = animals.map(animal => animal.emoji.repeat(animal.count)); ```
	- emojiZoo will now be a variable containing  an array of the emojis repeating based on the animal count
	- animals.map takes in a function: 
		- ``` animals.map(function(animal) { return animal.emoji.repeat(animal.count) }); ```
**Filter the Array**
- we can filter the array based on its values
- example: filter for animals that have 4 legs only
- ``` const fourLegsGood = animals.filter(animal => animal.legs == 4); ```
- **animal.legs == 4** is a boolean expression that, if true, will add it to the collection

**Find**
- looking up a single value in a collection
- ``` const cow = animals.find(animal => animal.name == 'Cow'); ```
- for each animal in animals, if animal.name == 'Cow' is true, it will return the FIRST object that matches, no subsequent matches
- find should be used on a primary key column 

**Includes**
- ``` if(animals.map(a => a.name).includes('Dragon')) {
			console.log("THERE BE DRAGONS HERE");
		} ```
- the if statement is successful because there are dragons

**Some**
- ``` const manaNeededToBattle = 40;
	if(animals.some(animal => animal.mana >= manaNeededToBattle)) {
			consol.log("We are ready!")
		} ```
- this returns as true

**Every**
- ``` if(animals.every(animal => animal.mana >= 40)) {
			console.log("We are ready!!");
		} ```
- this will return false! not every animal has mana greater than 40

**Reduce**
- Useful for a sum total or a sum over time, reduces a collection down to a single value
- Add up all the counts of the animals together:
	- ``` animals.reduce((total, animal) => total + animal.count, 0); ```
	- 0 represented the initial value, animal represents each object in the array

**Destructuring**
- ```🖤', '❤', '💛']; ```
- we can assign multiple variables on a single line of code instead of hearts[2] for red
- ``` const [black, red, yellow] = hearts; ```
- when naming just some, leave a blank: ``` const [black, , yellow] = hearts; ``` will name all but the red heart

**Key Value Pairs instead of Array Indexes**
- ```adventures() { mountain: '🗻', city: '🏙', desert: '🌵'}; ```
- we can assign these to values
- ``` const {mountain, desert} = adventures ```
- mountain will printout the emoji, it became a constant variable because it mapped
- renaming: ``` const {mountain: everest, desert: sahara} = adventures; ```
- sahara will be mapped to the result of desert, sahara has become the variable taking on the value of the key name desert

- ``` const anbimalFriends = [
		{ name: 'Monkey', emoji: '🐵'},
		{ name: 'Dog', emoji: '🐶'}],
		{ name: 'Cow', emoji: '🐮'}
	]; ```
- ``` const [ , {emoji: dogEmoji}] = animalFriends ```
- dogEmoji will be assigned 🐶

- ``` const apiResponse = {
				title: 'JS Environment',
				translations: [
							{
									locale: 'de - Germany',
									last_edit: '2014-04-14T08:43:37',
									title: 'JS Umgebung'
							}
				]
	}; ```
- want a variable containing the english and german title
- ``` let{
				title: englishTitle,
				translations:
						{title: germanTitle}
				]
	} = apiResponse; ``` 
- englishTitle and germanTitle have now been assigned!

#### Spread Operator

**Using Numbers**
- used in front of an array, it will expand the array and give it a comma separated value
- ``` console.log(Math.max(42, 56, 102, 12, 15)); ```
- ``` console.log(Math.max(...numbers)); ```
- the max will still come out without having to type the numbers (in an existing array, of course)

**CONACT -> Joining 2 arrays together**
- ``` litanyStart = ['Fear', 'is', 'the'];
      litanyEnd = ['mind', 'killer']; ```
- ``` const litanyFull = [...litanyStart, ...litanyEnd]; ```
- litanyFull will be a 5 object array
- ``` const middle = ['is', 'the]; 
	  const litany = ['Fear', ...middle, 'mind', 'killer']; ```
- litany will print out the full phrase

#### Destructuring and Spreading at once
- ``` const sentence = ['this', 'is', 'the', 'house', 'that', '🦆', 'built']; ```
- we can destructure and spread
- ``` const [first, second, ...theRest] = sentence; ```
- first = this, second = is, theRest = the whole rest of the sentence
- ``` theRest = 'the', 'house', 'that', '🦆', 'built']; ```

**With Key:Value Pairs**
- ``` const userSome = {fullName: 'Wally Glutton', age: 42};
	 const moarUser = {userName: 'stungeye', friend: 'Daisy'}; ```
- it isn't a different user, it's more of the same user, so we can join them
- ``` const userFull = { ...userSome, ...moarUser } ``` 
- userFull will contain all four of the properties
- want to combine data from two different data sets? you can do it here!

- ``` let book = {name: 'anathem', quote: 'Boredom is a mask frustration wears.'}; ```
- ``` book = { ...book, author: 'Neal Stephenson', quote: 'Topology is destiny.'}; ```
- we are inserting the author and overwriting the original quote, *be careful because the last thing you do will overwrite the previous thing*

- ``` function sayGoodnight(...names){
				const namesList = names.join(', ');
				console.log(`Goodnight ${namesList}!`);
		} ```
- here you can pass any sort of name into the parametre, even a spread
- ``` sayGoodnight('Wally', 'Daisy', 'Sammy'); ```
- will print Goodnight Wally, Daisy, Sammy!
