# Examples

The `docusign.dsadmin` connector provides practical examples illustrating usage in various scenarios. Explore these [examples](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples), covering use cases like permissions in organizations, and manage user information.

1. [Permissions in organizations](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples/permissions-in-organizations) - Manage and configure permission profiles for users within a DocuSign organization.

2. [Manage user information](https://github.com/ballerina-platform/module-ballerinax-docusign.dsadmin/tree/main/examples/manage-user-information) - Retrieve and update user details and settings within a DocuSign account.

## Prerequisites

1. Generate DocuSign credentials to authenticate the connector as described in the [Setup guide](https://central.ballerina.io/ballerinax/docusign.dsadmin/latest#setup-guide).

2. For each example, create a `Config.toml` file the related configuration. Here's an example of how your `Config.toml` file should look:

    ```toml
    token = "<Access Token>"
    ```

## Running an Example

Execute the following commands to build an example from the source:

* To build an example:

    ```bash
    bal build
    ```

* To run an example:

    ```bash
    bal run
    ```