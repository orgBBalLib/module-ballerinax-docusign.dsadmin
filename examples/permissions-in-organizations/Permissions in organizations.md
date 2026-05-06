# Permissions in Organizations

This example demonstrates how to manage users and retrieve permission profiles within a DocuSign organization using the DocuSign Admin API. The script fetches organizations, creates a new user, retrieves user information, and lists permission profiles and groups for a specific account.

## Prerequisites

1. **DocuSign Admin Setup**
   > Refer to the [DocuSign Admin setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest) to obtain OAuth2 credentials and configure your DocuSign developer account.

2. **Configuration**
   
   Create a `Config.toml` file in the project root directory with the following configuration:

   ```toml
   clientId = "<Your Client ID>"
   clientSecret = "<Your Client Secret>"
   refreshToken = "<Your Refresh Token>"
   refreshUrl = "<Your Refresh URL>"
   accountId = "<Your Account ID>"
   email = "<Your Email>"
   serviceUrl = "<Your Service URL>"
   ```

   | Configuration   | Description                                                    |
   |-----------------|----------------------------------------------------------------|
   | `clientId`      | OAuth2 client ID from your DocuSign application                |
   | `clientSecret`  | OAuth2 client secret from your DocuSign application            |
   | `refreshToken`  | OAuth2 refresh token for authentication                        |
   | `refreshUrl`    | Token refresh endpoint URL (e.g., `https://account-d.docusign.com/oauth/token`) |
   | `accountId`     | Your DocuSign account ID                                       |
   | `email`         | Email address for user lookup                                  |
   | `serviceUrl`    | DocuSign Admin API base URL (e.g., `https://api-d.docusign.net/management`) |

## Run the Example

Execute the following command to run the example. The script will print its progress to the console.

```shell
bal run
```

Upon successful execution, the script will:

1. Retrieve and display all organizations associated with your account
2. Create a new user within the first organization
3. Fetch and display user information for the specified email
4. List all permission profiles available in the account
5. Display all groups within the organization account