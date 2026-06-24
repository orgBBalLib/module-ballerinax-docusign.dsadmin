# Permissions in Organizations

This example demonstrates how to manage permissions and user information within DocuSign organizations using the DocuSign Admin API. The script retrieves organization details, creates a new user, fetches user information, and lists permission profiles and groups for an account.

## Prerequisites

1. **DocuSign Admin Setup**
   > Refer to the [DocuSign Admin setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest) to obtain OAuth2 credentials and configure your DocuSign developer account.

2. **Configuration**
   
   Create a `Config.toml` file in the project root directory with your DocuSign credentials:

   ```toml
   clientId = "<Your Client ID>"
   clientSecret = "<Your Client Secret>"
   refreshToken = "<Your Refresh Token>"
   refreshUrl = "<Your Refresh URL>"
   accountId = "<Your Account ID>"
   email = "<Your Email>"
   serviceUrl = "<Your Service URL>"
   ```

   > **Note:** You can also set these values as environment variables (`CLIENT_ID`, `CLIENT_SECRET`, `REFRESH_TOKEN`, `REFRESH_URL`, `ACCOUNT_ID`, `EMAIL`, `SERVICE_URL`) as the code supports reading from environment variables.

## Run the Example

Execute the following command to run the example. The script will perform the following operations and print the results to the console:

- Retrieve all organizations associated with the account
- Create a new user within the first organization
- Fetch user information for the specified email
- List all permission profiles for the account
- List all groups within the account

```bash
bal run
```