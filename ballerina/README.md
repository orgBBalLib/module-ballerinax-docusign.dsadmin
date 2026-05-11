## Overview

[DocuSign](https://www.docusign.com/) is a leading electronic signature and agreement management platform that enables organizations to securely sign, send, and manage documents digitally, accelerating business processes and eliminating paper-based workflows.

The `ballerinax/docusign.dsadmin` package offers APIs to connect and interact with [DocuSign Admin API](https://developers.docusign.com/docs/admin-api/) endpoints, specifically based on [DocuSign Admin API v2.1](https://developers.docusign.com/docs/admin-api/reference/).
## Setup guide

To use the DocuSign Admin connector, you must have access to the DocuSign Admin API through a [DocuSign developer account](https://developers.docusign.com/) and obtain an API access token. If you do not have a DocuSign account, you can sign up for one [here](https://go.docusign.com/o/sandbox/).

### Step 1: Create a DocuSign Account

1. Navigate to the [DocuSign Developer Center](https://developers.docusign.com/) and create a developer sandbox account, or log in if you already have one.

2. Note that the DocuSign Admin API requires an Organization-level account with Admin privileges. Access to the Admin API is available on DocuSign Enterprise plans or higher, and you must be an organization administrator to use the Admin API features.

### Step 2: Generate an API Access Token

1. Log in to your DocuSign developer account at the [DocuSign Developer Center](https://developers.docusign.com/).

2. Navigate to the **Settings** page by clicking on your profile icon in the top right corner.

3. Select **Apps and Keys** from the left navigation menu.

4. Click **Add App and Integration Key** to create a new application, or select an existing application.

5. Copy your **Integration Key** (Client ID) and configure your authentication method (either Authorization Code Grant or JWT Grant).

6. For quick testing, you can generate an access token by navigating to the **API and Keys** section and clicking **Generate Access Token** under the Actions menu for your application.

> **Tip:** You must copy and store this key somewhere safe. It won't be visible again in your account settings for security reasons.
## Quickstart

To use the `docusign.dsadmin` connector in your Ballerina application, update the `.bal` file as follows:

### Step 1: Import the module

```ballerina
import ballerina/oauth2;
import ballerinax/docusign.dsadmin as dsadmin;
```

### Step 2: Instantiate a new connector

1. Create a `Config.toml` file and configure the obtained credentials:

```toml
clientId = "<Your_Client_Id>"
clientSecret = "<Your_Client_Secret>"
refreshToken = "<Your_Refresh_Token>"
```

2. Create a `dsadmin:ConnectionConfig` and initialize the client:

```ballerina
configurable string clientId = ?;
configurable string clientSecret = ?;
configurable string refreshToken = ?;

final dsadmin:Client dsadminClient = check new ({
    auth: {
        clientId,
        clientSecret,
        refreshToken,
        refreshUrl: "https://account.docusign.com/oauth/token"
    }
});
```

### Step 3: Invoke the connector operation

Now, utilize the available connector operations.

#### Get a list of organizations

```ballerina
public function main() returns error? {
    dsadmin:OrganizationsResponse response = check dsadminClient->/v2/organizations.get();
}
```

### Step 4: Run the Ballerina application

```bash
bal run
```
## Examples

The `docusign.dsadmin` connector provides practical examples illustrating usage in various scenarios. Explore these [examples](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples), covering the following use cases:

1. [Permissions in organizations](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples/permissions-in-organizations) - Demonstrates how to manage and configure permissions within DocuSign organizations.
2. [Manage user information](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples/manage-user-information) - Illustrates how to retrieve, update, and manage user information in DocuSign Admin.