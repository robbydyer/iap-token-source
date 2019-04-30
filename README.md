
# iap-token-source

Go package that provides an [oauth2 token source](https://godoc.org/golang.org/x/oauth2#TokenSource) to use
for authentication to services secured with [Google Identity Aware Proxy](https://cloud.google.com/iap/docs/authentication-howto#authenticating_from_a_service_account).

## Status

Under development.  This has been tested with only a few IAP configurations.

## Usage

Note: this package only works with [Google Service Accounts](https://cloud.google.com/iam/docs/understanding-service-accounts)


This package can be used to authenticate HTTP and gRPC clients with [Google's Identity Aware Proxy](https://cloud.google.com/iap/) (better known as 
"IAP").

By default, the package uses [Application Default Credentials](https://cloud.google.com/video-intelligence/docs/common/auth#authenticating_with_application_default_credentials) - it will use the service account key at the path specified in the environment 
variable `GOOGLE_APPLICATION_CREDENTIALS`.

See the [gRPC](./examples/grpc/) and [HTTP](./examples/http/) examples for more information.