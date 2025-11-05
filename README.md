# MWAD-EXP_04-Simple-caluculator

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
Calculator.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator-container">
      <div className="calculator">
        <input type="text" value={input} readOnly className="display" />
        <div className="buttons">
          <button className="clear" onClick={handleClear}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>*</button>
          <button onClick={() => handleClick("-")}>-</button>

          {[7, 8, 9, 4, 5, 6, 1, 2, 3, 0].map((num) => (
            <button key={num} onClick={() => handleClick(num.toString())}>
              {num}
            </button>
          ))}

          <button onClick={() => handleClick("+")}>+</button>
          <button className="equal" onClick={handleCalculate}>=</button>
        </div>
      </div>
    </div>
  );
}

export default Calculator;
```
Calculator.css
```.calculator-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background-color: white;
}
.calculator {
  background-color: black;
  border-radius: 20px;
  padding: 20px;
  width: 280px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
}

.calculator {
  background-color: black;
  border-radius: 20px;
  padding: 20px;
  width: 280px;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
}

.display {
  width: 100%;
  height: 60px;
  background-color: #333;
  color: #00ff7f;
  border: none;
  border-radius: 10px;
  text-align: right;
  font-size: 24px;
  padding: 10px;
  margin-bottom: 15px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 55px;
  font-size: 20px;
  border: none;
  border-radius: 10px;
  background-color: #444;
  color: white;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}

button:hover {
  background-color: #666;
}

.clear {
  background-color: #e74c3c;
}

.clear:hover {
  background-color: #c0392b;
}

.equal {
  background-color: #2ecc71;
}

.equal:hover {
  background-color: #27ae60;
}
```
App.jsx
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <>
      <Calculator />
    </>
  );
}

export default App;
```

## OUTPUT

<img width="947" height="791" alt="image" src="https://github.com/user-attachments/assets/24310154-538e-4788-bb38-126348bf5a1a" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
