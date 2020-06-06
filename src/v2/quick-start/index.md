---
title: Quick Start
type: guide
order: 1
---

## Executive Overview
The way you use JuiceConfig will depend on your role in operations or as a developer. Generally the overall process will go as follows: 
1. Developers will define config parameters required for their application.
2. Operations will define environments and value of parameters supporting the application.
3. Juice assists with defining the parameter values for each environment, and save the resulting configs securely.
4. When retrieving previous configs, Juice pulls config values from secure storage (local or AWS/ECS/Docker).
### Example Use Case
There are 2 main usages for Juice:
* The local storage allows for development on your personal machine.
* Access to AWS, ECS and Docker allows deployment to these environments:
    * low security CI or test server
    * highly secure staging and production servers

## Config Manager
  * juiceconfig.com
     * non-secure values
  * self hosted
      * may contain secure values, if ...

## Defining a Configuration
  * dependancies
  * internal versus external values
  * Deployments

## Saving your config
  * flat files (JSON)
  * AWS Secrets Manager
  * Write your own plugin

## Accessing configs from files
  * NodeJS
  * Java (not ready yet)
  * Golang (not ready yet)

# CLI

## Updating legacy config files
e.g. Tomcat / Spring