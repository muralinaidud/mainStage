
## Prerequisites

- node
- npm
- git
- docker
- 
## Getting started

1. Create a personal access token in Gitlab, with no expiration date 
2. Run the following in your terminal:

```
npm config set '//gitlab.com/api/v4/packages/npm/:_authToken' "<access-token>"
Log in to your local computer as an administrator.
In a command prompt, run:
ssh-keygen -t rsa -C "your_email@example.com"
Associating the key with your email address helps you to identify the key later on.
Just press <Enter> to accept the default location and file name. If the .ssh directory doesn't exist, the system creates one for you.
Enter, and re-enter, a passphrase when prompted. The whole interaction will look similar to this:
```

3. clone the repository to your local machine (git@gitlab.com:t2803/io.git)
4. Run npm install to install dependencies.
5. Run npm run test (to run the test in terminal in headless mode)
6. Run npx cypress open (to run the test in terminal in head mode)


## Test scenarios implementation details

Current tests are developed using data driven framework

All the data for the test case to perform an actions as per the scenario is within fixtures folder functionalData.json file.

Base URL and Credentials are set in cypress.json

yml file is also been created to make the tests running on GitLab pipeline in a docker container

## Feature Enhancements

Current scripts did not used any reusable functions as this is just an assessment 

=> In order for us to reduce the number of lines of the code we can use reusable functions.
 
=> Current tests are not written using BDD(Cucumber framework) which can make tests more readable for non techenical persons as well.
   but set up is already done we shall directly start implementing

=> Current tests are designed in a scope to run the tests in multiple viewports like Desktop, Mobile, Tablet but our application doesn't seem like support anything
   other than desktop for now