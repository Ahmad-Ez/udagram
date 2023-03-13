# Hosting a Full-Stack Application (Udagram)


## Table of Contents
* [Description](#Descritpion)
* [Dependencies](#Dependencies)
* [Installation](#Installation)
* [Scripts](#Scripts)
* [Testing](#Testing)
* [Built With](<#Built with>)
* [License](#License)


## Description

The aim of this project is to apply the concepts of continous integration / continous deployment CI/CD to a full stack application (Udagram). The application source code was provided by Udacity as a part of the Full-Stack nanodegree program. 
This was achieved by utilizing the AWS solutions, namely AWS S3 for hosting the angular frontend, AWS EBS for the backend part powered by nodejs, and AWS RDS for hosting the postgres database of the app.

After the initial setup, the application needs to be deployed manually for the first time. Later, the process of code building, testing and deployment would be automated through CircleCI. This automation process is achieved by connecting the CircleCi web service to the Github repo containing the app source code, and with every new code push to the repo, a trigger is fired in CircleCI to the build, test, and deploy process.

Documentation covering the project are provided in the README.md files and in the docs folder.

 link to the hosted working Front-End Application [AppLink](http://udagram0126960145.s3-website-us-east-1.amazonaws.com/home)


## Dependencies

```
- Node v14.15.1 (LTS).

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- AWS RDS database running Postgres.

- AWS S3 bucket for hosting uploaded pictures.

```

## Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres.
1. In AWS, provision an S3 bucket for hosting the uploaded files.
1. Export the ENV variables needed to the CircleCI environment configuration.
1. From the root of the repo, navigate to the udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Scripts
- ```"frontend:install": "cd udagram/udagram-frontend && npm install -f"```  
Install the required package dependencies for the angular frontend app

- ```"frontend:start": "cd udagram/udagram-frontend && npm run start"```  
Start the frontend angular server

- ```"frontend:build": "cd udagram/udagram-frontend && npm run build"```  
Build the frontend app

- ```"frontend:test": "cd udagram/udagram-frontend && npm run test"```  
Run the frontend unit tests

- ```"frontend:e2e": "cd udagram/udagram-frontend && npm run e2e"```  
Run the e2e tests on the frontend app

- ```"frontend:lint": "cd udagram/udagram-frontend && npm run lint"```  
Lint the frontend app code

- ```"frontend:deploy": "cd udagram/udagram-frontend && npm run deploy"```  
Deploy the frontend app to the AWS S3 cloud

- ```"api:install": "cd udagram/udagram-api && npm install ."```  
Install the required package dependencies for the backend API

- ```"api:build": "cd udagram/udagram-api && npm run build"```  
Build the backend app

- ```"api:start": "cd udagram/udagram-api && npm run dev"```  
Start the backend server in the dev mode

- ```"api:deploy": "cd udagram/udagram-api && npm run deploy"```  
Deploy the back end app to the Elastic BeanStalk (EBS)

- ```"deploy": "npm run api:deploy && npm run frontend:deploy"```  
Deploy the frontend app to the AWS S3 cloud, and the backend to EBS

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## License

[License](LICENSE.txt)
