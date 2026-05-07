# Permissions in Organizations

This example demonstrates how to manage users and permissions within DocuSign organizations using the DocuSign Admin API. The script retrieves organization details, creates a new user, fetches user information, and lists permission profiles and groups associated with an account.

## Prerequisites

1. **DocuSign Admin Setup**
   > Refer to the [DocuSign Admin setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest) to obtain your OAuth2 credentials and configure your DocuSign developer account.

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
   | `clientId`      | OAuth2 client ID from your DocuSign app                        |
   | `clientSecret`  | OAuth2 client secret from your DocuSign app                    |
   | `refreshToken`  | OAuth2 refresh token for authentication                        |
   | `refreshUrl`    | Token refresh endpoint URL (e.g., `https://account-d.docusign.com/oauth/token`) |
   | `accountId`     | Your DocuSign account ID                                       |
   | `email`         | Email address for user lookup                                  |
   | `serviceUrl`    | DocuSign Admin API base URL (e.g., `https://api-d.docusign.net/management`) |

## Run the Example

Execute the following command to run the example. The script will print its progress to the console, displaying organization details, newly created user information, user lookup results, permission profiles, and groups.

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