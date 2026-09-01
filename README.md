# Ex04 Simple Calculator - React Project
## Date:14-03-2026
## Name : 
## Reg No :

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
APP.jsx
'''
import React, { useState } from "react";
import "./App.css";

function App() {
  const [display, setDisplay] = useState("");

  const handleClick = (value) => {
    setDisplay((prev) => prev + value);
  };

  const clearDisplay = () => {
    setDisplay("");
  };

  const calculate = () => {
    try {
      const result = eval(display);
      setDisplay(result.toString());
    } catch {
      setDisplay("Error");
    }
  };

  return (
    <div className="calculator-container">
      <div className="calculator">
        <h1>Simple Calculator</h1>

        <input
          type="text"
          value={display}
          readOnly
          className="display"
        />

        <div className="buttons">
          <button onClick={clearDisplay} className="clear">C</button>
          <button onClick={() => handleClick("/")}>÷</button>
          <button onClick={() => handleClick("*")}>×</button>
          <button onClick={() => handleClick("-")}>−</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={() => handleClick(".")}>.</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={calculate} className="equal">=</button>

          <button
            onClick={() => handleClick("0")}
            className="zero"
          >
            0
          </button>
        </div>
      </div>
    </div>
  );
}

export default App;
'''
APP.css
'''
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background: #1f2937;
}

.calculator-container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.calculator {
  width: 350px;
  padding: 25px;
  border-radius: 20px;
  background: #111827;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
}

.calculator h1 {
  color: white;
  text-align: center;
  margin-bottom: 20px;
  font-size: 26px;
}

.display {
  width: 100%;
  height: 70px;
  border: none;
  outline: none;
  border-radius: 10px;
  margin-bottom: 20px;
  padding: 10px 15px;
  text-align: right;
  font-size: 30px;
  background: #374151;
  color: white;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}

button {
  height: 60px;
  border: none;
  border-radius: 12px;
  font-size: 22px;
  font-weight: bold;
  cursor: pointer;
  background: #374151;
  color: white;
  transition: 0.2s;
}

button:hover {
  transform: scale(1.05);
  background: #4b5563;
}

.clear {
  background: #dc2626;
}

.equal {
  background: #16a34a;
  grid-row: span 2;
  height: 132px;
}

.zero {
  grid-column: span 3;
}

@media (max-width: 450px) {
  .calculator {
    width: 100%;
  }

  button {
    height: 55px;
  }
}
'''
## OUTPUT


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
