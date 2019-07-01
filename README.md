# SmartThingsAWSLambdaServerless
My attempt at creating an AWS Lambda integrated with SmartThings to augment my home automation.  Deploying with Serverless


## Steps to install:

- AWS CLI
  - set up credentials
- python3 
- NPM
- Serverless
-    Ensure AWS IAM permissions are set correctly


## Projects
1. Capture switch events from a [Shelly 1](https://shelly.cloud/shelly1-open-source/). 
After moving a door to a bedroom, I needed to locate a lightswitch near it.  I had access to main voltage, but no feed to the light itself.  The existing switch was already "smart" so I thought I could use a Shelly 1 to capture switch toggles and send the events to a smart hub.  But how to do it?
