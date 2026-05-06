# Manage User Information

This example demonstrates how to use the DocuSign Admin API to manage user information within an organization. The script retrieves organization details, creates a new user with account associations, and fetches user information from the organization.

## Prerequisites

1. **DocuSign Admin Setup**
   > Refer to the [DocuSign Admin setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest) to obtain your OAuth2 credentials and configure your DocuSign developer account.

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

Execute the following command to run the example. The script will print the organization details, newly created user information, and user information from the organization to the console.

```shell
bal run
```