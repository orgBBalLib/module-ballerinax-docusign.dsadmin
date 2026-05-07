## Overview

[DocuSign](https://www.docusign.com/) is a cloud-based electronic signature and agreement management platform that enables organizations to securely sign, send, and manage documents digitally, streamlining workflows and accelerating business transactions.

The `ballerinax/docusign.dsadmin` package offers APIs to connect and interact with [DocuSign Admin API](https://developers.docusign.com/docs/admin-api/) endpoints, specifically based on [DocuSign Admin API v2.1](https://developers.docusign.com/docs/admin-api/reference/).
## Setup guide

To use the DocuSign Admin connector, you must have access to the DocuSign Admin API through a [DocuSign developer account](https://developers.docusign.com/) and obtain an API access token. If you do not have a DocuSign account, you can sign up for a free developer account [here](https://go.docusign.com/o/sandbox/).

### Step 1: Create a DocuSign Account

1. Navigate to the [DocuSign Developer Center](https://developers.docusign.com/) and sign up for a free developer sandbox account or log in if you already have one.

2. Note that to use the DocuSign Admin API in production, your organization must have a DocuSign Organization with Admin functionality enabled, which requires an Enterprise plan or a plan that includes DocuSign Admin features.

### Step 2: Generate an API Access Token

1. Log in to your DocuSign developer account and navigate to the [Apps and Keys](https://admindemo.docusign.com/apps-and-keys) page in your eSignature Settings.

2. Click **Add App and Integration Key** to create a new application, then provide a name for your app.

3. Under your newly created app, note your **Integration Key** (Client ID) and generate a **Secret Key** by clicking **Add Secret Key**.

4. Configure your redirect URIs and authentication settings as needed for your application.

5. To obtain an access token, use the OAuth 2.0 authorization flow (Authorization Code Grant or JWT Grant) with your integration key and secret key through the DocuSign OAuth endpoints.

> **Tip:** You must copy and store this key somewhere safe. It won't be visible again in your account settings for security reasons.
## Quickstart

To use the `docusign.dsadmin` connector in your Ballerina application, update the `.bal` file as follows:

### Step 1: Import the module

```ballerina
import ballerina/oauth2;
import ballerinax/docusign.dsadmin;
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
        refreshUrl: "https://account.docusign.com/oauth/auth"
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
2. [Manage user information](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples/manage-user-information) - Illustrates retrieving, updating, and managing user information in DocuSign accounts.