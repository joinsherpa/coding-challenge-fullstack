# Full Stack Engineer Coding Challenge

Hello and welcome to the Full Stack Engineer coding challenge at sherpa°!

If you would rather show us something you have already worked on (either professionally, a side-project or from another interview), skip ahead to the Assessment section to ensure it covers the areas we want to see.

If you want to build something new, continue reading.

## Context

sherpa° sells visas to travellers to help them cross borders freely and efficiently. In order to help users find the visa they need to purchase, we need a *Products Application*. In this challenge we would like you to focus on either

1. **Full Stack Read-Only Feature**: Implementing a read product feature on both the client and server
2. **Frontend UI Feature with Mock API**: Implement a rich UI with a mock API for reading, sorting, filtering product info
3. **Server Read & Write Feature**: Implement an API to read, write and update product details

Each scenario is broken down further below. Pick the challenge which best exemplifies your skills and what you hope to do at sherpa°!

#### Scenario 1: Full Stack Read-Only Feature

Implement a feature both on the server and client to allow customers to 
- Read all products, with
    - Configurable [page](https://en.wikipedia.org/wiki/Pagination) sizes
    - Filters for X, Y, and Z
- Read a single product

Feel free to use your judgement on which data needs to rendered for the list and single product views. Loading and reading the data from a database is not necessary but will be great to see!

#### Scenario 2: Frontend UI Feature with Mock API

Implement a feature on the client to allow customers to 
- Read all products, with
    - Configurable [page](https://en.wikipedia.org/wiki/Pagination) sizes
    - Filters for price, fee, name, length of stay and number of entries
- Read a single product

Feel free to use your judgement on which data needs to rendered for the list and single product views. Given this scenario solely pertains to the front-end, feel free to mock the calls to the server and focus on accessibility and responsiveness to different screen sizes.


#### Scenario 3: Full Stack CRUD API with Database

Implement a feature on the server to allow customers to 
- Read all products, with
    - Configurable [page](https://en.wikipedia.org/wiki/Pagination) sizes
    - Filters for X, Y, and Z
- Read a single product
- Add a product
- Edit an existing product

Also, add a script to load the CSV data into the database.

This scenario expects you to use a database, we suggest [TypeORM](https://typeorm.io/) and SQLite. It also expects the data to be validated before saving.

## A note on AI

If you want to use AI, it is totally fine (we use it too...), we just want to know so we can ask questions about what worked, what didn't and how you would use it going forward.

## Components

In this repository, you will find an nx monorepo with

1. An Angular application
2. A Nest.JS application
3. A CSV file of product information

The above were kept lightweight on purpose so you can decide which tools to add if needed.

Lastly, feel free to add apps if you prefer to use a different framework, but make sure to set it up in Typescript.

### Data
Here is the product information as a CSV
```
Visa Name,Price (USD),Length of Stay (Days),Number of Entries,Filing Fee (USD)
Tourist Visa - USA,160,90,Single,20
Business Visa - USA,185,180,Multiple,25
Student Visa - USA,350,730,Multiple,50
Tourist Visa - Canada,100,180,Single,15
Business Visa - Canada,150,365,Multiple,30
Student Visa - Canada,200,1095,Multiple,40
Tourist Visa - UK,130,180,Single,25
Business Visa - UK,200,365,Multiple,35
Student Visa - UK,450,1095,Multiple,55
Schengen Visa - France,80,90,Single,10
Schengen Visa - Germany,90,90,Multiple,12
Schengen Visa - Italy,85,90,Single,11
Schengen Visa - Spain,88,90,Multiple,13
Tourist Visa - Australia,145,90,Single,18
Business Visa - Australia,250,365,Multiple,40
Student Visa - Australia,620,1095,Multiple,60
Tourist Visa - Japan,30,90,Single,8
Business Visa - Japan,55,180,Multiple,12
Student Visa - Japan,100,730,Multiple,25
Tourist Visa - China,140,90,Single,20
Business Visa - China,185,180,Multiple,30
Student Visa - China,250,1095,Multiple,45
Tourist Visa - India,25,30,Single,5
Business Visa - India,75,180,Multiple,10
Student Visa - India,100,365,Multiple,20
Tourist Visa - Brazil,40,90,Single,10
Business Visa - Brazil,160,180,Multiple,25
Student Visa - Brazil,200,730,Multiple,35
Tourist Visa - Russia,50,30,Single,15
Business Visa - Russia,150,180,Multiple,25
Student Visa - Russia,250,1095,Multiple,40
Tourist Visa - UAE,90,30,Single,10
Business Visa - UAE,120,180,Multiple,15
Student Visa - UAE,250,1095,Multiple,35
Tourist Visa - Mexico,36,180,Single,8
Business Visa - Mexico,100,365,Multiple,20
Student Visa - Mexico,200,1095,Multiple,30
Tourist Visa - South Africa,50,90,Single,12
Business Visa - South Africa,125,180,Multiple,18
Student Visa - South Africa,200,1095,Multiple,30
Tourist Visa - Argentina,150,90,Single,15
Business Visa - Argentina,180,180,Multiple,25
Student Visa - Argentina,250,1095,Multiple,35
Tourist Visa - Thailand,35,60,Single,5
Business Visa - Thailand,75,180,Multiple,10
Student Visa - Thailand,175,730,Multiple,25
Tourist Visa - Vietnam,25,30,Single,5
Business Visa - Vietnam,50,180,Multiple,12
Student Visa - Vietnam,150,730,Multiple,20
```

### React

```
npx nx add @nx/react
npx nx g @nx/react:application apps/react-client

npx nx run react-client:serve
```

### Node.js (Express, Fastify)

```
npx nx add @nx/node
npx nx g @nx/node:application apps/node-server

npx nx run node-server:serve
```

### Others

Many commonly used/supported frameworks can be found [here](https://nx.dev/nx-api).

## Setup

You should only need to run yarn to be ready for development.

```
npm i -g yarn # if you do not have yarn globally installed
yarn
```

## Running Locally

To run the client locally, run:
```
npx nx run client:serve
```

To run the server locally, run:
```
npx nx run server:serve
```

## Assessment

Rather than focusing on the completeness of the challenge, here are some of the areas we care about:
- **Testing**: did you implement tests? which kind and where? how well do they give us confidence that the code works as expected?
- **Typescript Use**: did you type your code well? does it give confidence that 
- **Code Organization**: how did you organize components and files and why? how might it affect the maintainability?
- **Code Readibility**: how did you name functions/variables? how do you structure a function or pass variables so it is easy to understand the purpose of the code?
- **Developer experience**: how well did you document the front-end or back-end so that another developer would be able to work on / integrate with your app(s)?
- **Tool/framework selection**: what tools did you add or use in your development and why? what are they good/bad at? what would you do differently in the future?
- **Logging**: how well do you implement logging to make your application maintainable and understandable? what tools would you use to help with logging?
- **Scaling**: how might you change your solution to handle millions of queries, users or products?
- **Documentation**: do you have documentation for your API? 
- **Errors**: how does your app handle errors (expected and unexpected)?


## Out of Scope Topics

We do not expect you to directly implement
- Authentication
- CI/CD and/or Deployment

but, if you want to we are happy to talk about it!