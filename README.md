# Postman Collection for using the Intelligent API

## Pre-requisites

1. Postman (https://www.postman.com/downloads/) installed

## How to use

### Environment Variables Setup

1. To begin ensure you have signed up at https://dash.intelligent-api.com and have generated at least one set of credentials (either a Basic or OAuth set of credentials).
2. Within Postman, select `Collections` and then `Import` and browse to and select the `intelligent-api.postman_environment.json` environment variables file.
3. Once the environment has been imported, select `Environments` within Postman and navigate to the `intelligent-api` environment.
4. If you have setup OAuth Credentials in Step 1, update the `clientId` and `clientSecret` values in the environment.
5. If you have setup Basic Credentials in Step 1, update the `basicAuthClientId` and `basicAuthClientSecret` values in the environment.
6. Ensure you save your changes before continuing.

### Using the OAuth Collection

1. If you have setup OAuth Credentials in Step 1 of the _Environment Variables Setup_ you will need to navigate back to `Collections` in Postman and then select `Import` again, and this time import the `Intelligent API.postman_collection.json` collection.
2. Once the collection has been imported, you will see the `Intelligent API` collection in your list of Postman collections.
3. Ensure you select the `intelligent-api` enviroment on the far top right drop down before starting to use the collection.
4. Once the collection has been imported and the environment has been selected, you should be able to begin by generating a `token` that you can use for subsequent API calls, to do this invoke the `02 Request Token` endpoint in the root of the `Intelligent API` collection.

> NB: When generating a token, you will only be able to specify `scopes` that the credentials you generated were granted access to when you creating them in the https://dash.intelligent-api.com dashboard. So for example if you created credentials and unticked some of the scopes, you cannot include those scopes when requesting a token.

5. This method will generate a token and place it into your environment variables for use with the rest of the endpoints, so once you have generated a token you will be able to invoke all the API endpoints the token has relevant scope to invoke for 4 hours before needing to generate a new token.
6. Once a token has been generated, you can invoke the remaining API endpoints as you wish.
7. The `Document` endpoints all require files as input, and to send a file to the endpoint simply select the `Body` tab, then select `binary` for the format and use the `Select File` input to browse for and select an appropriate file.

### Using the Basic Auth Collection

1. If you have setup Basic Credentials in Step 1 of the _Environment Variables Setup_ you will need to navigate back to `Collections` in Postman and then select `Import` again, and this time import the `Intelligent API - Basic Auth.postman_collection.json` collection.
2. Once the collection has been imported, you will see the `Intelligent API` collection in your list of Postman collections.
3. Ensure you select the `intelligent-api` enviroment on the far top right drop down before starting to use the collection.
4. Once the collection has been imported and the environment has been selected, you should be able to invoke any of the API endpoints.

> NB: When using `Basic Credentials`, you will only be able to invoke endpoints that the credentials were granted access to when you creating them in the https://dash.intelligent-api.com dashboard. So for example if you created credentials and unticked some of the scopes, you cannot invoke endpoints that require those scopes.

5. The `Document` endpoints all require files as input, and to send a file to the endpoint simply select the `Body` tab, then select `binary` for the format and use the `Select File` input to browse for and select an appropriate file.
