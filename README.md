# Fast-Food-Fast
[![Build Status](https://travis-ci.org/marcdomain/Fast-Food-Fast.svg?branch=develop)](https://travis-ci.org/marcdomain/Fast-Food-Fast) [![Coverage Status](https://coveralls.io/repos/github/marcdomain/Fast-Food-Fast/badge.svg?branch=develop)](https://coveralls.io/github/marcdomain/Fast-Food-Fast?branch=develop) [![Maintainability](https://api.codeclimate.com/v1/badges/2d74b6d3d4da8005455f/maintainability)](https://codeclimate.com/github/marcdomain/Fast-Food-Fast/maintainability)

## Description
Fast-Food-Fast​ is a food delivery service app for a restaurant.

<br/><b>UI-pages:</b> https://marcdomain.github.io/Fast-Food-Fast/UI
 <br/><b> API documentation: </b> https://marcus-fast-food-fast.herokuapp.com/api/v1/

## Features
Below are the features of Fast-Food-Fast Application at this point


###
- User can Signup <br>
- User can Login <br>
- Admin can post menu <br>
- User can get all available menu <br>
- User can post Orders to the app <br>
- User can get his/her order history<br/>
- Admin can also get order history of specific user <br>
- Admin can get all orders in the app <br>
- Admin can get a Specific order<br/>
- Update a specific order status
```
  Required Inputs
  {
    status:
  }
```
- Delete a specific order
<br/>

## API Endpoints

<table>

<tr><th>HTTP VERB</th><th>API ENDPOINT</th><th>FUNCTION</th><th>INPUT</th><th>OUTPUT</th></tr>

<tr>
<td>POST</td> <td>api/v1/auth/signup</td>  <td>Signup user</td>
<td>
{<br> name: "string",<br>email: "string",<br>phone: "string",<br> address: "string",<br>password: "string"<br>}
</td>
<td>
{<br> message: "string",<br>grabYourToken: "string"<br>}
</td>
</tr>

<tr>
<td>POST</td> <td>api/v1/auth/login</td>  <td>Login user</td>
<td>
{<br> email: "string",<br>password: "string"<br>}
</td>
<td>
{<br> message: "string",<br>grabYourToken: "string"<br>}
</td>
</tr>

<tr>
<td>POST</td> <td>api/v1/menu</td>  <td>Create new menu</td>
<td>
{<br> menu: "string",<br>description: "string",<br>category: "string",<br>quantity: "string",<br>price: "string"<br>}<br>token: "string" or authorization header
</td>
<td>{<br>message: "string"<br>menu: {object}<br>}</td>
</tr>

<tr>
<td>GET</td> <td>api/v1/menu</td>  <td>Get All Available Menu</td>
<td>token: "string" or authorization header</td>
<td>{<br>message: "string"<br>allMenu: {object}<br>}</td>
</tr>

<tr><td>POST</td> <td>api/v1/orders</td>  <td>Place order</td>
<td>{<br>menuId: "string",<br>quantity: "string",<br>location: "string" or undefined,<br>}<br>token: "string" or authorization header</td>
<td>{<br>message: "string"<br>}</td>
</tr>

<tr>
<td>GET</td> <td>api/v1/users/:userId/orders</td>  <td>Get user order history</td>
<td>userId: "Number"<br>token: "string" or authorization header</td>
<td>{<br>message: "string"<br>orderHistory: {object}<br>}</td>
</tr>

<tr>
<td>GET</td> <td>api/v1/orders</td>  <td>Get all orders</td>
<td>token: "string" or authorization header</td>
<td>{<br>message: "string"<br>allOrders: {object}<br>}</td>
</tr>

<tr>
<td>GET</td> <td>api/v1/orders/:orderId</td>  <td>Get specific order</td>
<td>token: "string" or authorization header</td>
<td>{<br>message: "string"<br>foundOrder: {object}<br>}</td>
</tr>

<tr><td>PUT</td> <td>api/v1/orders/:orderId</td> <td>Update an order status</td> <td></td> <td></td></tr>

<tr><td>DELETE</td> <td>api/v1/orders/:orderId</td> <td>Delete an order</td> <td></td> <td></td></tr>

</table>

## Installation
1. Clone this repository below:
```
https://github.com/marcdomain/Fast-Food-Fast
```
2. cd into the repository:
```
cd Fast-Food-Fast
```
3. Open the repository in terminal and Install dependencies by running:
```
npm install
```
4. Run "npm start" to start the app

5. Use Postman to test all endpoints

6. Run "npm test" to test all endpoints


## Technologies

ES6: See [here](https://en.wikipedia.org/wiki/ECMAScript) for details.

NodeJS: An open-source, cross-platform JavaScript run-time environment which allows you enjoy the features of Javascript off the web browsers and implement server-side web development. Visit [here](https://nodejs.org/en/) for details.

ExressJS: This is the web application framework for Node.js Visit [here](https://expressjs.com) for details.

Postgresql Database: PostgreSQL is a powerful, open source object-relational database system that uses and extends the SQL language combined with many features that safely store and scale the most complicated data workloads. Visit [here](https://www.postgresql.org/docs) for details.

Airbnb JavaScript style guide was adopted as a coding convention, see [here](https://github.com/airbnb/javascript) for details.


**_This project is under development phase. STAY TUNED_**
