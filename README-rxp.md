# RxP OpenAPI Spec; i.e., our API design spec 

Let's begin with a short intro from the OpenAPI Spec site: 

> The OpenAPI Specification (OAS) defines a standard, language-agnostic
> interface to RESTful APIs which allows both humans and computers to discover
> and understand the capabilities of the service without access to source code,
> documentation, or through network traffic inspection. When properly defined, a
> consumer can understand and interact with the remote service with a minimal
> amount of implementation logic.

> An OpenAPI definition can then be used by documentation generation tools to
> display the API, code generation tools to generate servers and clients in
> various programming languages, testing tools, and many other use cases.

In this directory, we use the OpenAPI Spec to write (by hand) a few YAML docs
that represent our API. Then, we use Swagger UI to read that spec. Swagger UI is
a tool that renders the spec into interactive browser documentation.

We use this spec to collaborate remotely on API design. Then, with Swagger UI we
allow API remote testing. Finally, we will use this spec to ensure that our
design aligns with the implementation, via contract testing. 

Okay, enough talk. Let's get rolling. 

## Dependancies 

- [node.js](https://nodejs.org/en/download/)
- [npm](https://www.npmjs.com/get-npm)

## Run Swagger UI to view the spec

```
$ npm install swagger-ui-watcher -g
```

## Deploy the spec

First, concat the various .yaml files into one file: 

xx

Then, commit your code and push: 

xx

Our GitHub workflow (xx link) takes care of the rest. 

We run the Swagger UI Docker container using GCloud's Cloud Run process: it
deploys a container in their cloud.

### Deployment caveats and details 

The GitHub action is dependant upon an image being available at `
gcr.io/rxpapi/swagger-ui`. We should probably change this: pull this image from
Docker Hub and push it to our GCloud registry.
