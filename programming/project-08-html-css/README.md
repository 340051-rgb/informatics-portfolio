# Project 3 – Auto Financing Simulator (HTML, CSS, JavaScript)

**Area:** Programming – Web Development  
**Level:** Intermediate  
**Year:** 2024  

## 1. Description

This project is a web-based auto financing simulator developed as a school practice project. The application allows users to simulate a vehicle financing plan by entering the vehicle name, price, down payment percentage, and financing term.
Although the project was not deployed to the web, it is fully functional in a local environment and focused on front-end logic, user interaction, and dynamic content generation using vanilla JavaScript.

## 2. Objective

To design and implement an interactive auto financing simulator using HTML, CSS, and JavaScript that calculates loan details, monthly payments, and generates a complete payment schedule based on user input.

## 3. Features

- Vehicle name input
- Vehicle price input
- Down payment selection (10%–50%)
- Financing term selection (12–60 months)
- Interest rate assignment using conditional logic
- Automatic calculation of:
  - Down payment amount
  - Financing amount
  - Monthly payment
- Dynamic generation of a payment schedule table including:
  - Payment number
  - Payment date
  - Payment amount

## 4. Technologies Used

- **HTML5**
  - Forms and input fields
  - Tables and select elements

- **CSS3**
  - Layout styling
  - Visual formatting using shadows, borders, and backgrounds

- **JavaScript (Vanilla)**
  - DOM access
  - Event handling
  - Conditional logic (`switch`)
  - Loops
  - Mathematical calculations
  - Date handling using `Date`

## 5. Project Structure

## 6. Code Explanation

### 6.1 User Input and Form Structure (HTML)

The project begins with an HTML form that collects all the necessary information to simulate an auto financing plan. The user enters the vehicle name and price and selects both the down payment percentage and the financing term using dropdown menus.

All inputs are grouped within a single form, allowing JavaScript to easily access user input values when the **“¡Cotiza tu crédito!”** button is clicked.

### 6.2 Event Handling and Data Collection (JavaScript)

When the user clicks the **“¡Cotiza tu crédito!”** button, the `cotiza()` function is executed. This function retrieves the values entered in the form and converts numeric inputs into integers using `parseInt()` so mathematical operations can be performed.

```js
precio = parseInt(carro.precio.value);
enganche = parseInt(carro.enganche.value);
meses = parseInt(carro.meses.value);

montoen = enganche / 100 * precio;
finan = precio - montoen;

switch (meses) {
  case 12: interes = 0; break;
  case 24: interes = 5; break;
  case 36: interes = 7; break;
  case 48: interes = 9; break;
  case 60: interes = 12; break;
}

var fecha = new Date();
hoy = fecha.getDate();
mes = fecha.getMonth() + 1;
año = fecha.getFullYear();

for (nump = 1, mes++; nump <= meses; nump++, mes++) {
  // Generates each payment row
}

