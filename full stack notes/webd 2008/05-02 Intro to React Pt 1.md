bind---
class: webd 2008
module:  module five
date:  2022-03-07
tags:  #webd-2008 #web-development #javascript #react
---

# Intro to React Part 1

### Javascript Frameworks

#### What are frameworks?
- they have changed how we write web applications
- frameworks try to make things a bit easier for us but we can perform more tasks in the browser itself
- we started to create single page applications but the view of the page changes even tho it's single page
- ember, angler, view, react, svelte...?

### codesandbox.io

**Dependencies**
- mvp.css automatically styles all the elements you have -> you can use import statments to add styles

- ``` const rootElement = document.getElementById("root");
	  ReactDOM.render(<App />, rootElement); ```
- render: this component, I want to render into that root element
- we are creating custom elements this way and displaying them out into the root element
- ``` const rootElement = document.getElementById("root");
	  ReactDOM.render(<p>Hello, World</p>, rootElement); ```
- this will just have a p tag with hello world because we are no longer using the app
- this is actually JSX, not HTML; this is a version of XML
	- XML is strict 

**Creating a Component and Function**
- ``` function Hello(){
  const name = "World";
  return <h2>Hello {name}</h2>;
}

import App from "./App";

const rootElement = document.getElementById("root");
ReactDOM.render(<Hello />, rootElement); ```
- <Hello /> actually calls the function here
- functions should be capitalized
- ``` import App from "./App"; ```
- when importing from a .js file, you don't need to type .js

- ``` export default function App() {
  return (
    <>
      <Hello />
    </>
  ); ```
  - the App() function is the parent function right now
- ***Empty Tags?***
	- we don't have to use divs all the time, we can use semantically relevant tags
	- empty tags are "fragment elements" that you can use in React: it creates a root element

**Overload Component**
- ``` function Hello(props) {
  return <h2>Hello {props.name}</h2>;
}

export default function App() {
  return (
    <>
      <Hello name="Allison" />
      <Hello name="Suho" />
      <Hello name="Sehun" />
    </>
  ); ```
  - now we've passed the parameter ***props*** for properties
  - ``` function Hello(props) {
  return <h2>{props.greeting} {props.name}</h2>;
}

export default function App() {
  return (
    <>
      <Hello name="Allison greeting="Hello" />
      <Hello greeting="Bonjour" name="Suho"  />
      <Hello name="Sehun" />
    </>
  );  ```
  - this will print out the greeting and then the name
  - even if a tag doesn't have the parameter, it will not result in an error, it will just print what is there

**Destructuring**
- ```function Hello({greeting, name}) {
  return <h2>{greeting} {name}</h2>;```
- you can add the value up top, or even default values
- ```function Hello({greeting = "Hello", name= "World"}) {
  return <h2>{greeting} {name}</h2>;```
- a tag with no values will now print out Hello World

#### Looping & Conditionals

**Loop Through an Array and Output**
- ```function Hello({ greeting, name }) {
  return (
    <h2>
      {greeting} {name}
    </h2>
  );
}

export default function App() {
  const names = ["Minseok", "Suho", "Baekhyun", "🐱‍🐉"];
  const helloComponents = names.map((name, i) => <Hello name={ name } />);

  return <>{helloComponents}</>;
}```
- here we have looped through the names within the hello function!
***An easier way that will work in restrict mode....***
- ```function Hello({ greeting, name }) {
  return (
    <h2>
      {greeting} {name}
    </h2>
  );
}

export default function App() {
  const names = ["Minseok", "Suho", "Baekhyun", "🐱‍🐉"];

  return (
    <>
      {names.map((name, i) => (
        <Hello name={name} key={i} />
      ))}
    </>
  );
}```
- have to interpolate and do it in one statement, it can be confusing and difficult to keep track of 

**DETAILS AND SUMNMARY TAGS**
- ``` 
function Region({region}){
return <sup>{region === "" ? "None" : region}</sup>;
}

function Country({country}){
const density = country.population / country.area;
const globalAverageDensity = 50;
const isDense = density > globalAverageDensity;
return(
			<details>
					<summary>
							<img src={country.flag} alt={country.name} /> [country.name}
					</summary>
					<p>
							<Region region={country.region}/>
							<sup>Population: {country.population}</sup>
							{isDense && <sup>Densely Populated</sup>}
					</p>
			</details>
		);
} ```
- details gives you the the click arrow to show the p tag, summary is tied into details in this instance
- **isDense &&** 
	- if it's dense, which is up top, then it will display the Densely Populated sup, if it's false, it will ignore everything after &&
- **Region function**
	- if the region is none, it will show "None"!
- <a href="https://3n330.csb.app/">LINK TO EXAMPLE</a>'