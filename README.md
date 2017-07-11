# Amazon Cognito Identity SDK for JavaScript for Node.js

This module was originally a forked from [amazon-cognito-identity-js](https://github.com/aws/amazon-cognito-identity-js) to [amazon-cognito-identity-js-node](https://github.com/kndt84/amazon-cognito-identity-js). I have since forked it again as the owner of the fork does not seem to be accepting pull requests.

I made updates to the codebase to sent a mock User Agent string in the HTTPS Requests, failure to do this causes errors like this: 
```shell
ReferenceError: navigator is not defined
    at CognitoUser.authenticateUserInternal (node_modules/amazon-cognito-identity-js/lib/CognitoUser.js:343:19)
```

## Install
```sh
npm install amazon-cognito-identity-js-node
```

## Usage
```sh
var AWS = require('aws-sdk');
var CognitoSDK = require('amazon-cognito-identity-js-node');

AWS.CognitoIdentityServiceProvider.AuthenticationDetails = CognitoSDK.AuthenticationDetails;
AWS.CognitoIdentityServiceProvider.CognitoUserPool = CognitoSDK.CognitoUserPool;
AWS.CognitoIdentityServiceProvider.CognitoUser = CognitoSDK.CognitoUser;
```
