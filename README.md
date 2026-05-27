# Ex04 Simple Calculator - React Project
## Date: 27.05.2026

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
### App.js
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return <Calculator />;
}

export default App;
```
### Calculator.js
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const click = (value) => {
    setInput(input + value);
  };

  const clear = () => {
    setInput("");
  };

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">

      <input type="text" value={input} readOnly />

      <div className="buttons">
        <button onClick={clear}>C</button>
        <button onClick={() => click("/")}>/</button>
        <button onClick={() => click("*")}>*</button>
        <button onClick={() => click("-")}>-</button>

        <button onClick={() => click("7")}>7</button>
        <button onClick={() => click("8")}>8</button>
        <button onClick={() => click("9")}>9</button>
        <button onClick={() => click("+")}>+</button>

        <button onClick={() => click("4")}>4</button>
        <button onClick={() => click("5")}>5</button>
        <button onClick={() => click("6")}>6</button>
        <button onClick={() => click("1")}>1</button>

        <button onClick={() => click("2")}>2</button>
        <button onClick={() => click("3")}>3</button>
        <button onClick={() => click("0")}>0</button>
        <button onClick={calculate}>=</button>
      </div>

    </div>
  );
}

export default Calculator;
```
### Calculator.css
```
.calculator {
  width: 250px;
  margin: 50px auto;
  padding: 20px;
  border: 2px solid black;
  text-align: center;
  background-color: white;
}

input {
  width: 100%;
  height: 40px;
  margin-bottom: 15px;
  border: 2px solid black;
  font-size: 24px;
  text-align: right;
  padding-right: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 10px;
}

button {
  height: 50px;
  background-color: black;
  color: white;
  border: none;
  font-size: 20px;
  cursor: pointer;
}

button:hover {
  opacity: 0.8;
}
```


## OUTPUT

<img width="1919" height="927" alt="image" src="https://github.com/user-attachments/assets/654f590d-d6b8-4eed-a13b-784b897f3fdc" />

<img width="1919" height="897" alt="image" src="https://github.com/user-attachments/assets/7d6cb0cf-3c9a-4305-8204-d1b086742fd9" />




## RESULT
The program for developing a simple calculator in React.js is executed successfully.
