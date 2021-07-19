# Nice Invoice

An easy and quick way to create an invoice. <br>

<img alt="npm" src="https://img.shields.io/npm/v/nice-invoice"><img alt="npm" src="https://img.shields.io/npm/dy/nice-invoice">


#### Preview - An example invoice

<img src="https://i.ibb.co/LnSK8rG/nice-invoice-3.png" alt="nice-invoice-2" border="0">

#### Features
 - Adjust Logo if available
 - Calculate price with quantity
 - Apply and calculate tax

## How to use it
Checkout <a href="https://medium.com/@devops6.01/a-nodejs-based-invoice-generator-package-370c2cda47f6">article</a>  for instllation or Following are quick steps for installing and using this package, 

### Step: 01
Install nice invoice package by following command. 

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
        quantity: 1,
        price: 50.00, 
        tax: "10%"
      },
      {
        item: "Watch",
        description: "Wall watch for office",
        quantity: 2,
        price: 30.00,
        tax: "10%"
      },
      {
        item: "Water Glass Set",
        description: "Water glass set for office",
        quantity: 1,
        price: 35.00,
        tax: ""
      }
    ],
    subtotal: 156,
    total: 156,
    order_number: 1234222,
    header:{
        company_name: "Nice Invoice",
        company_logo: "logo.png",
        company_address: "Nice Invoice. 123 William Street 1th Floor New York, NY 123456"
    },
    footer:{
      text: "This is footer - you can add any text here"
    },
    currency_symbol:"$", 
    date: {
      billing_date: "08 August 2020",
      due_date: "10 September 2020",
    }
};

niceInvoice(invoiceDetail, 'your-invoice-name.pdf');
```

### Optional Parameters 
Following parameters you can leave it blank, <br >
company_logo: ```company_logo: "",``` <br>
tax: ```tax: ""```

### Contributions

Contributions and suggestions are very welcome and wanted. I try to respond to pull requests within 24 hours, checkout <a href="https://github.com/bakhtawarshah/nice-invoice/blob/master/CONTRIBUTE.md">How to contribute</a>
