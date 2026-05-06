# Permissions in Organizations

This example demonstrates how to manage organizations and user permissions in DocuSign using the DocuSign Admin API. The script retrieves organizations, creates a new user, fetches user information, and lists permission profiles and groups within an organization.

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

   > **Note:** You can also set these values as environment variables (`CLIENT_ID`, `CLIENT_SECRET`, `REFRESH_TOKEN`, `REFRESH_URL`, `ACCOUNT_ID`, `EMAIL`, `SERVICE_URL`) as the code supports both configuration methods.

## Run the Example

Execute the following command to run the example. The script will print its progress to the console, displaying organization details, user creation results, user information, permission profiles, and groups.

```shell
bal run
```

Upon successful execution, you will see output similar to:

```
Organizations: {...}
New user created: {...}
User Information in the Organization: {...}
Permission Profiles: {...}
Groups: {...}
```