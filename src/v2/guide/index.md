---
title: juiceconfig.io
type: guide
order: 2
---

## Introduction
### What is Juice?
Juice is a configuration tool for AWS that assists programmers and non-programmers alike by creating a simple and intuitive process that ensures projects are managed effectively at each stage of development and deployed correctly every time. This system promotes security, transparency and consistency above all. 

### Why is it useful? 
Deployment can become a nightmare if your processes rely on individuals to maintain consistent and accurate configuration files. Most programmers develop their own procedures for deployment and storing sensitive information, and whilst companies may have recommended best practices, it’s easy for things to slip through the cracks due to human errors such as miscommunication, inexperience or just plain-old laziness. These mistakes are not only annoying but can pose serious security risks and can be damaging to client relationships. This is where Juice becomes a valuable asset in your future deployments.

Juice provides a simple, easy-to-use solution for configuring projects that prevents easily-made human errors. The procedure provided by Juice is safe guarded to prevent unauthorised personnel from making potentially damaging changes to existing infrastructure or projects. It also ensures that configuration files are consistent, thorough and values are recorded carefully and thoughtfully. 

### Is it secure?
Juice does not store or manage any sensitive information. During the project configuration process, Juice will request variable values for the project and each of its dependencies. This data is then stored in AWS Secrets Manager, or if preferable, in your local storage. Juice simply provides a safe-guarded procedure for recording configuration values that ensures smooth project deployment every time.

### Software license 
Juice is Public Domain and free to use... here's the software license info.... 

## Getting Started
### How to register
Your account will be registered using LoginService, a ToolTwist authentication tool. You can sign up using your email address or Facebook account. Simply create a password and a verification email will be sent to your inbox. Once verified you can login using the homepage at www.juiceconfig.io. 
 
<i>‘I forgot my password, what can I do?’</i> - Simply select the ‘forgot password’ option and a password reset will be sent to your designated email address or Facebook account. 

### Setting up your account
#### Understanding your intended use
Juice can be used by individuals or businesses, and the way that you set up your account will reflect this. If you are looking to set up a personal account to create a stream-lined process but do not need to include other users, simply register at the login page and set a password, then confirm your account via email. As a business, you will need to set up the account as a superuser, then add in users manually and individually select their accessibility for each deployable and environment once the account has been set up. 

#### Getting to know the layout
There will be a variety of familiar terms you will see on the website. To avoid confusion, make sure you understand what they require before entering in any data: 

Glossary | Description
------------- | -------------
Deployables  | Deployables are programs that can be either existing projects or software that the projects require to run (such as mySQL, ContentService or LoginService).
Project  | A project is a program that is in the process of development. Not all deployables will be projects. 
Dependencies | Dependencies are deployables that are required to run exisiting projects and other deployables. For example, a project might require LoginService and ContentService to run, therefore they would be the projects dependencies. A dependency might also have its own dependencies, which would be declared on its own deployables page.
Environments | Environments are exactly as you would imagine, they can be on a local server or on a pre-setup server. 
Variables | Variables are the configurable values that are required for each project to be deployed (such as endpoints or database name). Variables should be created for every deployable and their dependencies, and each variable will be given values when configuring a project. 

#### Adding data
The rest is intuitive and the process of adding information is up to you. However, generally we might suggest the following order:  (This will include screen shots as a guide, once the UI is ready)
1. Your first step might be to add the deployables. Depending on how complicated or numerous your programs are, this might take a while. Alternatively you may wish to add all deployables relevant to a certain project, then go through the entire process for each project to ensure that you do not miss any dependencies (deployables) for that project. 
2. Next, you should populate the relevant fields for each deployable. This includes entering in the deployables variables and dependencies. You should have all deployables added already, so adding dependencies is as simple as selecting the deployable from a list.
3. Adding environments will be the simplest part of the process. Simply add the names and specifications of your environments.
4. Next add the names and roles for users who will need access to Juice. The users tab will only be viewable for the superuser or read/write users. This displays a list of all users with access to your Juice account, their accessibility which can be edited, and the projects and environments that they are involved in. 
5. Lastly, as a superuser you will need to manually add users to each project or environment, or create read/write access for other users so that they can add themselves and members of their team to projects and environments where applicable. However, it is important to make sure that limited users have read/write access to minimise the chances of human error.

{% raw %}
<br>
<br>
<div style="max-width: 600px;">
  <img style="width: 100%;" src="../../images/diagram.png">
</div>
{% endraw %}

<!-- #### Settings
Lastly, you can manage your account by clicking on the settings tab in the top right-hand corner.  -->

### How to configure a project for deployment
Once your project has made it through development and testing, you’ll need to think about deploying it with AWS. Using Juice, configuring and storing variable values is as easy as this:

No details on this section yet… so here is some speculation… (Later this will also show screen shots of the process to guide)
1. To configure a project, first you need to select the deployable in the relevant environment and select ‘configure’. This will bring you to a screen that displays the projects variables and the dependencies' variables. You will need to fill in <u>all</u> fields, then click send. 
2. Juice will then connect to AWS Secrets Manager where you will be required to provide authorisation before storing the variable values. 

And that’s it. Super simple, super intuitive. 
Good luck and happy coding!