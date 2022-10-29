# movinsync
const express = require('express');
const app=express();

const customers = [
    {custId: 1, customerName: 'chin',email: 'c333@gmail.com',mobileNo:'6538263287',city: 'Patna'},
    {custId: 2, customerName: 'neel',email: 'n222@gmail.com',mobileNo:'9852748955',city: 'Chennai'},
    {custId: 3, customerName: 'ayush',email: 'a444@gmail.com',mobileNo:'9966452846',city: 'Delhi'}
]

app.get('/', (req, res) => {
    res.send('Hello world');
})

app.get('/customers', (req, res) => {
    res.send(customers);
})


const port = process.env.PORT || 3000;
app.listen(port, () => console.log(`Listening on port ${port}`));

