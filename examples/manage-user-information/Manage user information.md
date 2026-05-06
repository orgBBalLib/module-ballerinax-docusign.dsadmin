# Manage User Information

This example demonstrates how to manage user information in DocuSign using the DocuSign Admin API. The script retrieves organization details, creates a new user within an organization, and fetches user information from the organization.

## Prerequisites

1. **DocuSign Setup**
   > Refer to the [DocuSign setup guide](https://github.com/ballerina-platform/ballerina-library/blob/main/packages/docusign/dsadmin/Package.md#setup-guide) to obtain OAuth2 credentials and configure your DocuSign developer account.

2. **Configuration**
   
   Create a `Config.toml` file in the project root directory with your DocuSign credentials:

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

   > **Note:** The configuration values can also be set as environment variables (`CLIENT_ID`, `CLIENT_SECRET`, `REFRESH_TOKEN`, `REFRESH_URL`, `ACCOUNT_ID`, `USER_ID`, `EMAIL`, `SERVICE_URL`).

## Run the Example

Execute the following command to run the example. The script will print organization details, create a new user, and display user information to the console.

```shell
bal run
```