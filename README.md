# Ex04 Simple Calculator - React Project

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


 # App.css
 ```
.calculator {
  width: 300px;
  margin: 30px auto;
  padding: 20px;
  border: 2px solid #444;
  border-radius: 10px;
  text-align: center;
  background: #f9f9f9;
}

input[type="text"] {
  width: 90%;
  height: 40px;
  font-size: 24px;
  margin-bottom: 15px;
  text-align: right;
  padding: 5px;
}

.buttons button {
  width: 60px;
  height: 50px;
  font-size: 20px;
  margin: 5px;
  cursor: pointer;
}

footer {
  margin-top: 20px;
  font-size: 14px;
  color: #666;
}
```

# App.js

```
import React from "react";
import Calculator from "./Calculator";
import "./App.css";

function App() {
  return (
    <div className="App">
      <Calculator />
    </div>
  );
}

export default App;
```

# Calculator.js 
```
import React, { useState } from "react";

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
      // eslint-disable-next-line no-eval
      const result = eval(input);
      setInput(result.toString());
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h1>Simple Calculator</h1>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("+")}>+</button>
        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("-")}>-</button>
        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={handleClear}>C</button>
        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={handleCalculate}>=</button>
        <button onClick={() => handleClick("/")}>/</button>
      </div>
      <footer>
        DIVYA M   212223040043
      </footer>
    </div>
  );
}

export default Calculator;
```

## OUTPUT
<img width="1868" height="875" alt="Screenshot 2025-09-12 132551" src="https://github.com/user-attachments/assets/3fb9519e-b7fc-4666-9742-aa07e70cfc6c" />

<img width="1861" height="921" alt="Screenshot 2025-09-12 132604" src="https://github.com/user-attachments/assets/b717de7b-e10b-4a55-9ae8-4265c985d81f" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
