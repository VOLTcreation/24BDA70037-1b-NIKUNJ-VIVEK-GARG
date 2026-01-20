# 24BDA70037-1B – Nikunj Vivek Garg

 Simple Banking UI – Responsive Web Application


## Project Overview

This project is a simple and responsive banking user interface developed using HTML, CSS, and JavaScript.
It allows users to deposit and withdraw money while displaying the updated balance instantly.
The interface is designed using a mobile-first approach so that it works smoothly on mobile phones, tablets, and desktop screens.

## Objectives of the Project

1. To design a clean and user-friendly banking interface
2. To implement deposit and withdrawal functionality
3. To validate user input before processing transactions
4. To make the application fully responsive across devices

---

## Technologies Used

1. HTML5 for structure and layout
2. CSS3 for styling and responsive design
3. JavaScript for logic and interactivity

---

## Project Structure**

The project consists of the following files:

1. index.html
   Defines the structure of the banking interface.

2. styles.css
   Handles the layout, colors, fonts, and responsiveness of the UI.

3. script.js
   Contains the logic for balance updates, deposits, withdrawals, and validations.


**HTML Implementation** (index.html)

The HTML file provides a semantic and accessible structure for the application.
It includes a balance display, an input field for amount entry, and buttons for deposit and withdrawal.

Code Snippet:

```html
<main class="banking-container">
  <h1 id="balance-display" class="balance-display">₹0.00</h1>

  <form class="banking-form">
    <label for="amount">Amount</label>
    <input type="number" id="amount" placeholder="Enter amount" />

    <div class="actions">
      <button type="button">Deposit</button>
      <button type="button">Withdraw</button>
    </div>
  </form>
</main>
```

---

*CSS Implementation* (styles.css)

The CSS file is responsible for visual styling and responsiveness.
A mobile-first approach is used along with Flexbox, Grid, and media queries.

Key Features of Styling:

1. Centered layout using Flexbox
2. Responsive container using max-width
3. Grid-based button layout
4. Media queries for tablets and desktops

Code Snippet:

```css
.banking-container {
  width: 100%;
  max-width: 420px;
  background: white;
  padding: 30px;
  border-radius: 10px;
}

.actions {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
}

@media (min-width: 600px) {
  .actions {
    grid-template-columns: 1fr 1fr;
  }
}
```

---

**JavaScript Functionality** (script.js)

JavaScript is used to handle the banking logic.

Main Responsibilities:

1. Store and update the account balance
2. Handle deposit and withdrawal actions
3. Validate user input
4. Display error messages when needed

Implementation Approach:

1. Read the entered amount from the input field
2. Check if the value is valid and greater than zero
3. Update the balance based on the selected action
4. Display the updated balance instantly

---

Responsive Design Explanation

The application is fully responsive due to the following reasons:

1. Mobile-first CSS design
2. Flexible widths instead of fixed values
3. Grid layout that adapts to screen size
4. Media queries for larger screens

The UI adjusts automatically for:

1. Mobile devices
2. Tablets
3. Laptops
4. Desktop screens



## ***Glossary of Terms***

**General Programming Terms**

1. UI – User Interface
   The visual part of an application that users interact with.

2. Responsive Design
   A design approach that ensures a website works on all screen sizes.

3. Validation
   The process of checking whether user input is correct.

4. Logic
   The set of rules that control how a program works.

---

**JavaScript Abbreviations**

1. JS – JavaScript
2. DOM – Document Object Model
3. API – Application Programming Interface
4. UI – User Interface

---

**CSS Abbreviations**

1. CSS – Cascading Style Sheets
2. RGB – Red Green Blue
3. px – Pixel
4. vh – Viewport Height
5. vw – Viewport Width

---

**HTML Abbreviations**

1. HTML – HyperText Markup Language
2. URL – Uniform Resource Locator
3. ID – Identifier
4. Meta – Metadata
