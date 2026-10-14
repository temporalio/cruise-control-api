# Temporal Cruise Control API

## How to use

To use the Cruise Control API in your project, preform the following 4 steps:
1. Copy over the protobuf files under [temporal](temporal) directory to your desired project directory
2. Use [gRPC](https://grpc.io/docs/) to compile and generate code in your desired programming language, typically handled as a part of your code build process
3. Create a client connection in your code using a Temporal Cloud API Key (see [Samples](#samples) below)
4. Use the Cruise Control API services to automate Cruise Control Operations, such as setting up pipelines or publishing artifacts

### API Version

The client is expected to pass in a `temporal-api-version` header with the api version identifier with every request it makes to the apis. The backend will use the version to safely mutate resources. The `temporal:versioning:min_version` label specifies the minimum version of the API that supports the field.

Current Version `v0.1.0`

### URL

The gRPC URL the clients should use to connect you can get from the Temporal Cloud console.
