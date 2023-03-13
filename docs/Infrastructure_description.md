# Hosting a Full-Stack Application (Udagram)

The application has three main components:

## AWS RDS database:  
A public postgres database instance, with proper configuration to allow inbound connections from the API.

## AWS Elastic BeanStalk app:  
A Nodejs express API, which accepts requests from the frontend app and communicates with the RDS database. [AppLink](http://udagram-api-dev3214352.us-east-1.elasticbeanstalk.com/)


## AWS S3 bucket:  
A dedicated bucket, for hosting the angular frontend app and the uploaded files. It's optimized to allow for web hosting and accept ACLs to allow deployment via AWS CLI. [AppLink](http://udagram0126960145.s3-website-us-east-1.amazonaws.com/home)