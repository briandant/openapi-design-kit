## OpenAPI design starter kit

A kit to collaboratively design an OpenAPI spec.  For more context, see [this
blog post](https://briandant.com/20200629--an-openapi-devkit/).

## get started

### install the prereqs 

- [nodejs and npm](https://nodejs.org/en/download/)
- `$ npm install swagger-ui-watcher -g`

### clone it and start watching your spec 

- `$ git clone git@github.com:briandant/openapi-design-kit.git`
- `$ swagger-ui-watcher ./openapi.yaml`

Your browser will open to `localhost:8000`.

- Edit your spec: this root dir contains your entrypoint `openapi.yaml`.

Here are some sections to pay attention to:

* Top-level **description**: this accepts markdown, and Redoc and Redocly API
  Reference will render it at the top of the docs.  Consider maintaining your
  markdown in a separate file and [embedding
  it](https://docs.redoc.ly/api-reference-docs/embedded-markdown/). Note to
  Redoc community edition users, the special tags are only available to the
  Redocly API Reference users, but you can still embed markdown.
* Security schemes: you will define the scheme(s) your API uses for security (eg
  OAuth2, API Key, etc...). The security schemes are used by the Redocly API
  Reference "Try It" API console feature.
* [Paths](paths/README.md): this defines each endpoint.  A path can have one
  operation per http method.
* Tags: it's a good idea to organize each operation.  Each tag can have a
  description.  The description is used as a section description within the
  reference docs.
* Servers: a list of your servers, each with a URL.

## deploy it 

TODO

# projects 

This kit is built on: 

- [swagger-ui-watcher](https://www.npmjs.com/package/swagger-ui-watcher
- [Redocly](https://redoc.ly/) 
- [Redoc](https://github.com/Redocly/Redoc)
- [create-openapi-repo](https://github.com/Redocly/create-openapi-repo)
