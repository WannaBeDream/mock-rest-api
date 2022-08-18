## Mock Rest API based on yaml/json file

# Usage steps
1. `npm i`
2. `npm run tern-on-api`

# Overview
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |


# Task
1. Test pagination, by way like `http://localhost:3000/users?page=1&pageSize=2`. 
2. Test sorting, by way like `http://localhost:3000/users?sortOrder=ASC&sortKey=firstName`. You can sort an any resource response using query parameters sortOrder and sortKey.
3. Test status code for REST API (200,400 and so on).
4. Test response time.
5. Test response thanks to json schema validation (optional).
5. Try to follow `AAA` approach (arrange, act, assert). 

# Testing tools

1. You can use one from following tools:
- <a href="https://github.com/WannaBeDream/jest-axios-openapi"> axios+jest boilerplate </a> (<a href="https://axios-http.com/docs/intro"> axios docs</a> & <a href="https://jestjs.io"> jest docs </a>)
- <a href="https://www.npmjs.com/package/supertest"> supertest.js </a>
- <a href="http://dareid.github.io/chakram/"> chakram.js </a>
- another one solution
2. Don't forget to add Reporter(ex. Allure).
3. Inject report into GH pages thanks to GH actions.

