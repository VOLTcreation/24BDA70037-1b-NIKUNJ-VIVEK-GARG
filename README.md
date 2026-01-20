# 24BDA70037-1B – Nikunj Vivek Garg

 Simple Banking UI – Practical Implementation

## 1. Aim of the Experiment

The aim of this experiment is to design and develop a Simple Banking User Interface using HTML, CSS, and JavaScript. The application allows users to view their account balance, perform deposit and withdrawal operations, validate user inputs, and store balance data persistently using browser storage.

## 2. Software and Tools Used

HTML5 is used to create the structure of the application.
CSS3 is used for styling and making the interface responsive.
JavaScript (ES6) is used to implement application logic and interactivity.
Browser localStorage is used to store balance data.
VS Code is used as the code editor.
Google Chrome is used for testing and debugging.

## 3. Project Description

This project represents a basic banking system interface developed using front-end web technologies. The application starts with a default balance and allows the user to deposit or withdraw money. All validations are performed on the client side. The balance is stored using localStorage, ensuring that the data remains available even after the page is refreshed or the browser is reopened.

## 4. Project Folder Structure

```
Simple-Banking-UI/
│
├── index.html      – Defines the structure of the user interface
├── styles.css      – Handles styling and responsiveness
├── script.js       – Contains application logic
└── README.md       – Project documentation
```

## 5. Implementation Details

### 5.1 HTML Implementation (index.html)

The HTML file provides the basic structure of the banking interface.

#### Balance Display

```html
<h1 id="balance-display" class="balance-display">
  Balance: $1000
</h1>
```

This element displays the current account balance. It is dynamically updated using JavaScript whenever a transaction occurs.

---

#### Amount Input Field

```html
<input
  type="number"
  id="amount"
  class="input-field"
  step="0.01"
/>
```

This input field allows the user to enter an amount for deposit or withdrawal. The step attribute enables decimal values.

---

#### Action Buttons

```html
<button type="button" onclick="handleDeposit()">
  Deposit
</button>

<button type="button" id="withdraw-btn">
  Withdraw
</button>
```

The deposit button directly calls a JavaScript function, while the withdraw button is handled using an event listener.

---

#### Error Message

```html
<p id="error-message" class="error-message">
  Invalid amount!
</p>
```

This element is used to display error messages such as invalid input or insufficient balance.

---

### 5.2 CSS Implementation (styles.css)

CSS is used to design a clean and user-friendly interface.

#### CSS Variables

```css
:root {
  --primary-blue: #1e40ff;
  --error-red: #dc3545;
}
```

CSS variables are defined to manage colors efficiently and make future design changes easier.

#### Input Validation Styling

```css
.input-field.valid {
  border-color: #22c55e;
}
```

When the user enters a valid amount, the input field border turns green to provide visual feedback.

#### Responsive Design

```css
@media (min-width: 480px) {
  .banking-container {
    width: calc(100% - 52px);
  }
}
```

Media queries are used to ensure that the interface adapts properly to different screen sizes.


### 5.3 JavaScript Implementation (script.js)

The JavaScript file controls the functionality and behavior of the application.

### Balance Initialization and Storage

```javascript
let balance =
  parseFloat(localStorage.getItem("bankBalance")) || 1000;
```

The balance is retrieved from localStorage if available. If no saved value exists, a default balance of 1000 is assigned.

---

#### Updating the Balance

```javascript
function updateBalance() {
  balanceDisplay.textContent = `Balance: ${balance}`;
  localStorage.setItem("bankBalance", balance);
}
```

This function updates the balance shown on the screen and saves the updated value in localStorage.

---

#### Input Validation

```javascript
function validateAmount(amount) {
  return amount > 0 && !isNaN(amount);
}
```

This function ensures that the entered amount is a valid positive number.

---

#### Deposit Functionality

```javascript
function handleDeposit() {
  const amount = parseFloat(amountInput.value);

  if (validateAmount(amount)) {
    balance += amount;
    updateBalance();
    amountInput.value = "";
  } else {
    showError();
  }
}
```

The deposit logic validates the input, adds the amount to the balance, updates the display, and clears the input field.

---

#### Withdrawal Functionality

```javascript
withdrawBtn.addEventListener("click", () => {
  const amount = parseFloat(amountInput.value);

  if (amount > balance) {
    errorMessage.textContent = "Insufficient funds!";
  } else {
    balance -= amount;
    updateBalance();
  }
});
```

This logic prevents overdrawing the account and displays an error message if the balance is insufficient.

---

#### Real-Time Input Feedback

```javascript
amountInput.addEventListener("input", () => {
  if (validateAmount(amount)) {
    amountInput.classList.add("valid");
  }
});
```

As the user types, the input is validated in real time and visual feedback is provided.

---

## 6. Features Implemented

Deposit functionality
Withdrawal functionality
Input validation
Error handling
Real-time balance updates
Persistent storage using localStorage
Responsive user interface

---

## 7. Result

The application successfully performs deposit and withdrawal operations with proper validation. The account balance remains stored even after refreshing the page.

## 8. Glossary of Terms

**General Programming Terms**

User Interface (UI) – The visual part of an application that users interact with
Local Storage – Browser feature used to store data persistently
Event Handler – A function that runs in response to user actions
Responsive Design – Designing layouts that adapt to different screen sizes

**JavaScript Abbreviations**

JS – JavaScript
DOM – Document Object Model
NaN – Not a Number
API – Application Programming Interface

**CSS Abbreviations**

CSS – Cascading Style Sheets
PX – Pixels
REM – Root Em unit
FR – Fractional unit used in CSS Grid
Media Query – CSS rule used for responsive design

**HTML Abbreviations**

HTML – HyperText Markup Language
DOCTYPE – Document Type Declaration
UTF – Unicode Transformation Format
ID – Identifier