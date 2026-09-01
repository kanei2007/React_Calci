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
APP.js
'''
 import { useState } from "react";
import "./App.css";

function App() {
  const [display, setDisplay] = useState("");

  const handleClick = (value) => {
    setDisplay(display + value);
  };

  const calculate = () => {
    try {
      setDisplay(eval(display).toString());
    } catch {
      setDisplay("Error");
    }
  };

  const clearDisplay = () => {
    setDisplay("");
  };

  return (
    <div className="page">

      <div className="calculator">
        <h1>Simple Calculator</h1>

        <input
          type="text"
          value={display}
          readOnly
          className="display"
        />

        <div className="buttons">
          <button className="clear" onClick={clearDisplay}>C</button>
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

          <button className="equal" onClick={calculate}>=</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>

          <button className="zero" onClick={() => handleClick("0")}>0</button>
          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>

      <footer>
        Designed by Kaneimozhi | 212224040147
      </footer>

    </div>
  );
}

export default App;     
'''
APP.css
'''
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #283cba, #7045a5);
  padding: 20px;
}

.calculator {
  width: 330px;
  padding: 24px;
  border-radius: 18px;
  background: #1d1f20;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.35);
}

h1 {
  text-align: center;
  color: white;
  font-size: 30px;
  margin: 0 0 20px;
}

.display {
  width: 100%;
  height: 65px;
  border: none;
  border-radius: 10px;
  background: #292c2d;
  color: white;
  font-size: 28px;
  text-align: right;
  padding: 10px;
  margin-bottom: 18px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 9px;
}

button {
  height: 58px;
  border: none;
  border-radius: 11px;
  background: #303334;
  color: white;
  font-size: 21px;
  font-weight: bold;
  cursor: pointer;
}

button:hover {
  background: #414445;
}

.clear {
  background: #d00000;
}

.clear:hover {
  background: #ed1111;
}

.equal {
  background: #2140c4;
  grid-row: span 2;
}

.equal:hover {
  background: #3154e0;
}

.zero {
  grid-column: span 2;
}

footer {
  margin-top: 20px;
  color: white;
  font-size: 15px;
  text-align: center;
  font-weight: 500;
}
'''
## OUTPUT
<img width="937" height="910" alt="Screenshot 2026-09-01 214212" src="https://github.com/user-attachments/assets/b36c1af2-7236-4b3a-b30e-2ce5a458f51f" />
<img width="945" height="912" alt="Screenshot 2026-09-01 214417" src="https://github.com/user-attachments/assets/e9ee1071-bb9c-4911-a650-68cde1aef2a9" />
<img width="946" height="916" alt="Screenshot 2026-09-01 214423" src="https://github.com/user-attachments/assets/bffc4012-6485-4279-ba86-67748dd9b42a" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
