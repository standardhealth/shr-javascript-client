# shr-javascript-client
JavaScript client implementation of shr-rest-api

## Generating Code
Code in the `javascript-client` directory was generated using the Swagger Online Editor (https://editor.swagger.io/).

If an updated swagger.json or swagger.yaml file is defined, a new JavaScript client implementation will need to be generated. It can be generated using the Swagger Online Editor or other Swagger tools. The new JavaScript implementation should replace the `javascript-client` directory.

## Update NPM Package
The `javascript-client` library is published on NPM as a package called `shr_rest_client`. This allows it to be saved on other projects and used to make REST API calls.

When changes are made to the `javascript-client` library, the updates should always be updated to the published NPM Package. Instructions for updating an NPM Package can be found [here](https://docs.npmjs.com/getting-started/publishing-npm-packages#updating-the-package);

## Manual Edits to Generated Code
In order to run this code using Webpack, the code in `javascript-client` directory that uses AMD was commented out. See the javascript-client README.md file for further details.

This implementation is used in Flux Notes, which is part of the Standard Health Record Collaborative. This project is still in development and will continue evolving. In order for this project to be compatible with Flux, the API call in `javascript-client/src/api/DefaultApi.js` was changed to be synchronous. If a new implementation is generated and the synchronous code is still needed, the following code can replace the API call in DefaultApi.js:

```
// Synchronous call
// TODO: This should be replaced with the above code, which was generated and is async
var xmlHttp = new XMLHttpRequest();
xmlHttp.open("GET", 'http://localhost:3001/api/patient/-1', false);
xmlHttp.send(null);
return xmlHttp.responseText;
```