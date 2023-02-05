**javascript object destructure examples with details commenting:**  

  
```
`// Destructuring an array`  

`const numbers = [1, 2, 3, 4, 5];`  

`const [first, second, ...rest] = numbers;`  

`// first variable is assigned the value of numbers[0] = 1`  

`// second variable is assigned the value of numbers[1] = 2`  

`// rest variable is assigned the value of numbers.slice(2) = [3, 4, 5]`  

`// Destructuring an object`  

`const person = {`   

`name: 'John Doe',`   

`age: 32,`   

`address: {`   

`city: 'New York',`   

`state: 'NY'  }};`  

`const { name, age } = person;`  

`// name variable is assigned the value of person.name = 'John Doe'`  

`// age variable is assigned the value of person.age = 32`  

`const { address: { city } } = person;`  

`// city variable is assigned the value of person.address.city = 'New York'`  

`// Destructuring with default values`  

`const { occupation = 'Unknown' } = person;`  

`// occupation variable is assigned the value of person.occupation if it exists, otherwise 'Unknown'`  
```
  

  

**rename city to mycity :**  
```
`const person = {`   

`name: 'John Doe',`   

`age: 32,`   

`address: {`   

`city: 'New York',`   

`state: 'NY'  }};`  

`const { address: { city: myCity } } = person;`  

`// myCity variable is assigned the value of person.address.city = 'New York'`  
```
  

  

**destructure from req object in one nested object destructuring :**  
```
`const express = require('express');`  

`const router = express.Router();`  

`router.post('/:id', (req, res) => {`   

`/ Destructure all properties from req.params, req.user, and req.body in one nested destructuring`   

`const {`   

`params: { id },`   

`user: { name, email },`   

`body: { description = '', price = 0 }  } = req;`   

`// Use the destructured values in your logic`   

``console.log(`Updating product with id ${id}`);``   

``console.log(`User details: ${name} (${email})`);  console.log(`Product description: ${description}`);  console.log(`Product price: ${price}`);``   

`// Return a response`   

`res.send('Product updated successfully');});`  

`module.exports = router;`  

  ```

  

  

  

**rename the id to jobId :**  

`const express = require('express');`  

`const router = express.Router();`  

`router.post('/:id', (req, res) => {`   

`/ Destructure all properties from req.params, req.user, and req.body in one nested destructuring`   

`const {`   

`params: { id:jobId },`   

`user: { name, email },`   

`body: { description = '', price = 0 }  } = req;`   

`// Use the destructured values in your logic`   

``console.log(`Updating product with id ${id}`);``   

``console.log(`User details: ${name} (${email})`);``   

``console.log(`Product description: ${description}`);``   

``console.log(`Product price: ${price}`);``   

`// Return a response`   

`res.send('Product updated successfully');});`  

`module.exports = router;`
