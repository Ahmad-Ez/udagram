# Hosting a Full-Stack Application (Udagram)


## Table of Contents
* [Description](#Descritpion)
* [Scripts](#Scripts)
* [Usage](#Usage)
* [Dependencies](#Dependencies)


## Description

The aim of this project is to apply the concepts of continous integration / continous deployment CI/CD to a full stack application (Udagram). The application source code was provided by Udacity as a part of the Full-Stack nanodegree program. 
This was achieved by utilizing the AWS solutions, namely AWS S3 for hosting the angular front end, AWS EBS for the backend part powered by nodejs, and AWS RDS for hosting the postgres database of the app.

After the initial setup, the application needs to be deployed manually for the first time. Later, the process of code building, testing and deployment would be automated through CircleCI. This automation process is achieved by connecting the CircleCi web service to the Github repo containing the app source code, and with every new code push to the repo, a trigger is fired in CircleCI to the build, test, and deploy process.

Documentation and runbooks covering the project are provided in the README.md files and in the docs folder.

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
