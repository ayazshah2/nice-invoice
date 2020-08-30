# Nice Invoice

An easy and quick way to create an invoice.
<br ><br >
<img alt="npm" src="https://img.shields.io/npm/v/nice-invoice">
<img alt="npm" src="https://img.shields.io/npm/dy/nice-invoice">

## How to use it
Following are quick steps for installing and using this package, 

### Step: 01
Install nice invoice package by following command 

```npm i nice-invoice```

### Step: 02
Include package main class into your page
```
const niceInvoice = require("nice-invoice");
```
### Step: 03
Store your invoice details into variable and then generate it. 

```   
  const invoiceDetail = {
    shipping: {
      name: "Micheal",
      address: "1234 Main Street",
      city: "Dubai",
      state: "Dubai",
      country: "UAE",
      postal_code: 94111
    },
    items: [
      {
        item: "Chair",
        description: "Wooden chair",
        quantity: 2,
        price: 50.00, 
        tax: "10%"
      },
      {
        item: "Watch",
        description: "Wall watch for office",
        quantity: 1,
        price: 70.00,
        tax: "10%"
      }
    ],
    subtotal: 120,
    total: 120,
    order_number: 1234222,
    header:{
        company_name: "Nice Invoice Company",
        company_logo: "logo.png",
        company_address: "Nice Invoice. 123 William Street 1th Floor New York, NY 123456"
    },
    footer:{
      text: "Any footer text - you can add any text here"
    },
    currency_symbol:"$", 
    date: {
      billing_date: "08 August 2020",
      due_date: "10 September 2020",
    }
};

niceInvoice(invoiceDetail, 'your-invoice-name.pdf');
```
