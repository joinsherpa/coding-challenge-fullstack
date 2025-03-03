# Full Stack Engineer Coding Challenge

Hello and welcome to the Full Stack Engineer coding challenge at sherpa°!

If you would rather show us something you have already worked on (either professionally, a side-project or from another interview), skip ahead to the Assessment section to ensure it covers the areas we want to see.

If you want to build something new, prepare to send no more than 3 hours on the below challenge.

## Context

sherpa° sells visas to travellers to help them cross borders freely and efficiently. In order to help users find the visa they need to purchase, we need a *Products Application*. In this challenge we would like you to build a server and client to complete the following features.

- Read all products (paginated and filtered by price, fee, name, length of stay and/or number of entries)
- Read a single product
- Edit a single product
- Add a new product

We do not expect you to complete all of the above features, so feel free to decide if you want to focus more on building a complete and robust RESTful API or a responsive/accessible user interface. Use your discretion on how much effort to spend on testing (unit, integration, etc.), but ensure that you at least integrate the server and client.

## Components

In this repository, you will find an nx monorepo with

1. An Angular application
2. A Nest.JS application
3. A CSV file of product information [(documented below)](#data)

The above were kept lightweight on purpose so you can decide which tools to add if needed.

Lastly, feel free to change the frameworks if you prefer, but make sure to set it up in Typescript.

### To Add a React App

```
npx nx add @nx/react
npx nx g @nx/react:application apps/react-client

npx nx run react-client:serve
```

### To Add a Node.js App (Express, Fastify)

```
npx nx add @nx/node
npx nx g @nx/node:application apps/node-server

npx nx run node-server:serve
```

### Others

Many commonly used/supported frameworks can be found [here](https://nx.dev/nx-api).

## Data
Here is the product information as a CSV
```
Country,Visa Type,Price (USD),Length of Stay (Days),Number of Entries,Filing Fee (USD)
USA,Tourist,160,90,Single,20
USA,Business,185,180,Multiple,25
USA,Student,350,730,Multiple,50
Canada,Tourist,100,180,Single,15
Canada,Business,150,365,Multiple,30
Canada,Student,200,1095,Multiple,40
UK,Tourist,130,180,Single,25
UK,Business,200,365,Multiple,35
UK,Student,450,1095,Multiple,55
France,Schengen,80,90,Single,10
Germany,Schengen,90,90,Multiple,12
Italy,Schengen,85,90,Single,11
Spain,Schengen,88,90,Multiple,13
Australia,Tourist,145,90,Single,18
Australia,Business,250,365,Multiple,40
Australia,Student,620,1095,Multiple,60
Japan,Tourist,30,90,Single,8
Japan,Business,55,180,Multiple,12
Japan,Student,100,730,Multiple,25
China,Tourist,140,90,Single,20
China,Business,185,180,Multiple,30
China,Student,250,1095,Multiple,45
India,Tourist,25,30,Single,5
India,Business,75,180,Multiple,10
India,Student,100,365,Multiple,20
Brazil,Tourist,40,90,Single,10
Brazil,Business,160,180,Multiple,25
Brazil,Student,200,730,Multiple,35
Russia,Tourist,50,30,Single,15
Russia,Business,150,180,Multiple,25
Russia,Student,250,1095,Multiple,40
UAE,Tourist,90,30,Single,10
UAE,Business,120,180,Multiple,15
UAE,Student,250,1095,Multiple,35
Mexico,Tourist,36,180,Single,8
Mexico,Business,100,365,Multiple,20
Mexico,Student,200,1095,Multiple,30
South Africa,Tourist,50,90,Single,12
South Africa,Business,125,180,Multiple,18
South Africa,Student,200,1095,Multiple,30
Argentina,Tourist,150,90,Single,15
Argentina,Business,180,180,Multiple,25
Argentina,Student,250,1095,Multiple,35
Thailand,Tourist,35,60,Single,5
Thailand,Business,75,180,Multiple,10
Thailand,Student,175,730,Multiple,25
Vietnam,Tourist,25,30,Single,5
Vietnam,Business,50,180,Multiple,12
Vietnam,Student,150,730,Multiple,20
```

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

## Running into Issues

If you have any issues with the above documentations, please contact us as soon as possible!

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

## A note on AI

If you want to use AI, it is totally fine (we use it too...), we just want to know so we can ask questions about what worked, what didn't and how you would use it going forward.

## Out of Scope Topics

We do not expect you to directly implement
- Authentication
- CI/CD and/or Deployment
- Wireframes/Prototypes Documentation

but, if you want to we are happy to talk about it!