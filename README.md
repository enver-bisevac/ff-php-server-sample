# Before you Begin

Harness Feature Flags (FF) is a feature management solution that enables users to change the software’s functionality, without deploying new code. FF uses feature flags to hide code or behaviours without having to ship new versions of the software. A feature flag is like a powerful if statement.

For more information, see https://harness.io/products/feature-flags/

To read more, see https://ngdocs.harness.io/category/vjolt35atg-feature-flags

To sign up, https://app.harness.io/auth/#/signup/

This is a sample app demonstrating PHP Server SDK integration with Relay Proxy.

## To use this application, follow the steps as below ##

1) [Create a project](https://ngdocs.harness.io/article/1j7pdkqh7j-create-a-feature-flag#step_1_create_a_project) in Harness with Feature-flags module enabled
2) [Create an environment](https://ngdocs.harness.io/article/1j7pdkqh7j-create-a-feature-flag#step_2_create_an_environment) within your project
3) Create a server and client side sdk keys in your environment and copy to clipboard
4) Rename .env.example to .env
5) Set environment variables:
- ACCOUNT_IDENTIFIER - Go to Account settings/Overview section in admin panel and copy Account Id
- ORG_IDENTIFIER -
- ADMIN_SERVICE=https://uat.harness.io/gateway/cf
- ADMIN_SERVICE_TOKEN - [Create service account and create a token](https://ngdocs.harness.io/article/tdoad7xrh9-add-and-manage-api-keys#create_service_account_token)
- CLIENT_SERVICE=http://config.feature-flags.uat.harness.io/api/1.0
- SDK_BASE_URL=https://config.feature-flags.uat.harness.io/api/1.0
- SDK_EVENTS_URL=https://event.feature-flags.uat.harness.io/api/1.0
- API_KEYS - [You need to provide server key](https://ngdocs.harness.io/article/1j7pdkqh7j-create-a-feature-flag#step_3_create_an_sdk_key)
- SDK_KEY - [You need to provide client key](https://ngdocs.harness.io/article/1j7pdkqh7j-create-a-feature-flag#step_3_create_an_sdk_key)
6) Create a boolean [feature-flag](https://ngdocs.harness.io/article/1j7pdkqh7j-create-a-feature-flag) in the admin console
7) Replace the values for SDK Key (client) and feature-flag identifier in the example program from step 3 and 4
8) Run the environment with `make start` and open [link](http://localhost:8080/) with sample response

## Stop all services

```shell
make stop
```