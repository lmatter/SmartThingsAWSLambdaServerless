# SmartThingsAWSLambdaServerless
My attempt at creating an AWS Lambda integrated with SmartThings to augment my home automation.  Deploying with Serverless.  Note that I'm doing this on Ubuntu 18.04 running inside Windows Services for Linux (WSL).  WSL 2 had a bad timezone bug so I rolled back to WSL1


## Steps to install:

- python3 
- AWS CLI
  - pip3 install awscli
  - .aws/{credentials,config}
  - no space between params and equals sign or you get java null pointer from some tools.
- NPM
- Serverless
  - https://serverless.com/blog/framework-example-golang-lambda-support/  
  - Ensure AWS IAM permissions are set correctly


## Projects
1. Capture switch events from a [Shelly 1](https://shelly.cloud/shelly1-open-source/). 
After moving a door to a bedroom, I needed to locate a lightswitch near it.  I had access to main voltage, but no feed to the light itself.  The existing switch was already "smart" so I thought I could use a Shelly 1 to capture switch toggles and send the events to a smart hub.  But how to do it?

## WSL Notes
https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly
