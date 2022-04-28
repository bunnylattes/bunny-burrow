---
class: webd 2008
module:  module five
date:  2022-03-07
tags:  #webd-2008 #web-development #javascript #react
---

# Intro to React Part 2

<a href="https://bit.ly/3goZGrX">***LINK TO THE TEMPLATE FOR THE VIDEO***</a>

### Events & State

- ``` function ClickMe() {
			  function handleClick() {
				    alert("Hello Clicker!");
			  }

			  return <button onClick={handleClick}>Click Me 👆</button>;
				}

export default function App() {
  return (
    <>
      <ClickMe />
    </>
  );
}```
- functions within functions are good and okay, especially if it's just used in that instance

**Anonymous Function**
- ``` function ClickMe() {
  return <button onClick={() => alert("Hewwo Inliner")}>Click Me 👆</button>;
}```

#### Events

- ``` function Events() {
  function handleClick(event) {
    event.preventDefault();

    alert("No visit for you to " + event.target.href);
  }
  return (
    <div>
      <a href="https://google.ca" onClick={handleClick}>
        This link has been hijacked!
      </a>
    </div>
  );
}

export default function App() {
  return (
    <>
      <Events />
    </>
  );
}```
- the function handleClick has the event passed through, prevents the default event from being performed, and displays an alert with the link concatinated on

#### States

**Getter and Setters -> Setters Re-Rendering a Component's State**
- React uses a HOOK to allow you access to intermediary events; things that happen in the lifecycle of the application, you can quickly pull out of the code and interject somecode.

**Use State Hook**
- ```import React, { useState } from "react";```
- this imports the useState function returns a two element array that we can destructure into a getter and a setter
- ```function ClickCounter() {
  const [count, setCount] = useState(0);

  return <button onClick={() => setCount(count + 1)}>Clicks: {count} 👆</button>;
}

export default function App() {
  return (
    <>
      <ClickCounter />
    </>
  );
}```
- this uses the state of the array: the click object is updated with every click from the starting value of 0

**Immutable**: State cannot change. You cannot say count++,  you must use the setter (setCount and useState in this case)

- ```const [count, setCount] ```
- whatever you named your immutable variable (count), you just put set in front of it to make a setter

- ```function UpBoats() {
  const [count, setCount] = useState(0);
  const boats = count < 0 ? count : "🚤".repeat(count);

  return (
    <div>
      <h2>Boats: {boats}</h2>
      <button onClick={() => setCount(count - 1)}>👎</button>
      <button onClick={() => setCount(0)}>Reset</button>
      <button onClick={() => setCount(count + 1)}>👍</button>
    </div>
  );
}```
- make the boats repeat with each click of the thumbs up

#### Forms

**Data Binding**
- using an onChange event, we can bind data for example:
- ``` function Mirror() {
  const [text, setText] = useState("On the wall");

  function inputChanged(event) {
    setText(event.target.value);
  }
  return (
    <div>
      <input onChange={inputChanged} value={text} />
      <button>Clear Input</button>
      <p>Mirror Mirror: {text}</p>
    </div>
  );
}

export default function App() {
  return (
    <>
      <Mirror />
    </>
  );
}```
- in this, the data will show after Mirror Mirror: (the text)

#### CSS In React

- ```function ToggleButton() {
  const [toggle, setToggle] = useState(false);
  const buttonClass = toggle ? "on" : "off";

  return (
    <button className={buttonClass} onClick={() => setToggle(!toggle)}>
      Using ClassName: {buttonClass}
    </button>
  );
}

export default function App() {
  return (
    <>
      <ToggleButton />
    </>
  );
}```
- ```button.on {
  background-color: #7d3c98;
  border: 2px solid #7d3c98;
}

button.off {
  background-color: #1d8348;
  border: 2px solid #1d8348;
}```
- changes the class of the button through an onClick event

**CSS Within Javascript in React**
- ```function ToggleButton() {
  const buttonStyle = {
    backgroundColor: "rgb(215, 85, 15",
    border: "none",
    fontSize: "40px",
    height: "200px",
    width: "200px",
  }
  return <button style={buttonStyle}>Styled Button</button>;
}

export default function App() {
  return (
    <>
      <ToggleButton />
    </>
  );
}```


- ```  <label>
                <input type="checkbox" />
                {toDo.text}
              </label>```
- this will put the check boxes and text attached


