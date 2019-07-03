# SmartThings - AWS Lambda integration using Serverless 
My attempt at creating an AWS Lambda integrated with SmartThings to augment my home automation.  Lamdas are written in Go ([golang](https://golang.org)), deploying with [Serverless](https://serverless.com).  Note that I'm doing this on Ubuntu 18.04 running inside Windows Services for Linux (WSL).  WSL 2 had a bad timezone bug so I rolled back to WSL1

These notes are crytptic while I'm still figuring out how to do this (don't want documentation to be a barrier), but feel free to reach out to me with any questions you may have.  
## Steps to install:

- python3 
- go
  - untar in ~/.local for easy upgrades.
- AWS CLI
  - pip3 install awscli
  - .aws/{credentials,config}
  - no space between params and equals sign or you get java null pointer from some tools.
- Lambda
  - The most important page I found.  https://community.smartthings.com/t/while-creating-smartapp-it-response-with-error-code-422/147806/3
- NPM
- Serverless
  - https://serverless.com/blog/framework-example-golang-lambda-support/  
  - Ensure AWS IAM permissions are set correctly
  - Guard against https://forum.serverless.com/t/framework-is-ignoring-profile-aws-account-settings-per-stage-profile/4613/5
  - SmartThings
    - This might be easiest example:  https://github.com/derekpovah/aws-lambda-st-iot-button


## Projects
1. Capture switch events from a [Shelly 1](https://shelly.cloud/shelly1-open-source/). 
After moving a door to a bedroom, I needed to locate a lightswitch near it.  I had access to main voltage, but no feed to the light itself.  The existing switch was already "smart" so I thought I could use a Shelly 1 to capture switch toggles and send the events to a smart hub.  But how to do it?

## WSL Notes
https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly
