# Manage User Information

This example demonstrates how to manage user information in DocuSign using the DocuSign Admin API. The script retrieves organizations, creates a new user within an organization, and fetches user information based on account and email filters.

## Prerequisites

1. **DocuSign Setup**
   > Refer to the [DocuSign setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest) to obtain OAuth2 credentials and configure your DocuSign developer account.

2. **Configuration**
   
   Create a `Config.toml` file in the project root directory with your credentials:

   ```toml
   clientId = "<Your Client ID>"
   clientSecret = "<Your Client Secret>"
   refreshToken = "<Your Refresh Token>"
   refreshUrl = "<Your Refresh URL>"
   accountId = "<Your Account ID>"
   userId = "<Your User ID>"
   email = "<Your Email>"
   serviceUrl = "<Your Service URL>"
   ```

   > **Note:** You can also set these values as environment variables (`CLIENT_ID`, `CLIENT_SECRET`, `REFRESH_TOKEN`, `REFRESH_URL`, `ACCOUNT_ID`, `USER_ID`, `EMAIL`, `SERVICE_URL`) as the code reads from environment variables with `os:getEnv()`.

## Run the Example

Execute the following command to run the example. The script will print its progress to the console, including organization details, the newly created user information, and user details retrieved from the organization.

```shell
bal run
```