# Project 3 – Auto Financing Simulator (HTML, CSS, JavaScript)

**Area:** Programming – Web Development  
**Level:** Intermediate  
**Year:** 2024  

## 1. Description

This project is a web-based auto financing simulator developed as a school practice project. The application allows users to simulate a vehicle financing plan by entering the vehicle name, price, down payment percentage, and financing term.
Although the project was not deployed to the web, it is fully functional in a local environment and focused on user interaction and dynamic content generation using JavaScript.

## 2. Objective

To design and implement an interactive auto financing simulator using HTML, CSS, and JavaScript that calculates loan details, monthly payments, and generates a complete payment schedule based on user input.

## 3. Technologies Used

- **HTML**
- **CSS**
- **JavaScript**

## 4. Code Explanation

### 4.1 User Input and Form Structure (HTML)

The project begins with an HTML form that collects all the necessary information to simulate an auto financing plan. The user enters the vehicle name and price and selects both the down payment percentage and the financing term using dropdown menus.

### 4.2 Event Handling and Data Collection (JavaScript)

When the user clicks the **“¡Cotiza tu crédito!”** button, the `cotiza()` function is executed. This function retrieves the values entered in the form and converts numeric inputs into integers using `parseInt()` so mathematical operations can be performed.

```js
precio = parseInt(carro.precio.value);
enganche = parseInt(carro.enganche.value);
meses = parseInt(carro.meses.value);
```
### 4.3 Financial Calculations

The script calculates the down payment amount and the total financing amount based on the selected percentage.

```js
montoen = enganche / 100 * precio;
finan = precio - montoen;
```
An annual interest rate is assigned using a `switch` statement depending on the selected financing term.

```js
switch (meses) {
  case 12: interes = 0;
  break;
  case 24: interes = 5;
  break;
  case 36: interes = 7;
  break;
  case 48: interes = 9;
  break;
  case 60: interes = 12;
  break;
}
```
This structure allows the application to clearly apply different interest rates depending on the financing duration.

### 4.4 Date Handling

The project uses JavaScript’s `Date` object to obtain the current date, wich is displayed as the contract signing date.

```js
var fecha = new Date();
hoy = fecha.getDate();
mes = fecha.getMonth() + 1;
año = fecha.getFullYear();
```

### 4.5 Payment Schedule Generation

A `for` loop dynamically generates the payment schedule table. Each iteration represents one monthly payment and includes: 

- Payment number
- Payment date
- Monthly payment amount

```js
for (nump = 1, mes++; nump <= meses; nump++, mes++) {
  // Generates each payment row
}
```
This logic allows the application to create a complete payment table based on user-selected financing terms.

### 4.6 Dynamic Content Rendering

After form submission, the result page is dynamically generated using JavaScript. The application displays: 

- Vehicle Information
- Financing summary
- Interest rate
- Monthly payment
- Complete payment schedule

This approach allows the user to immediately see the results without navigating to a new page.

### 4.7 Styling and Layout (CSS)

CSS is used to style the form, buttons, and tables using:

- Rounded borders
- Shadows
- Background images
- Consistent typography

### 7. Challenges and Solutions
