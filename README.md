# OpenAPI Flask Generaotr Template

This repository extends the python-flask templates of `openapi-generator-cli` with following.

- Flask-SQLAlchemy
- Flask-Migrate
- flask-marshmallow
- marshmallow-sqlalchemy
- schemathesis

## Setup

```bash
npm install @openapitools/openapi-generator-cli
```

## Generate server codes

```bash
openapi-generator-cli generate -i openapi.yml -g python-flask -t templates/server -o server -c config.yml
```

## Run the flask server with debug mode

```bash
cd server
flask --app openapi_server run -p 8080 --debug
```

## Test server codes

```bash
cd server
tox
```

## Edit `.openapi-generator-ignore`

Edit `.openapi-generator-ignore' to prevent some files from being overwritten.

```
openapi_server/test
git_push.sh
openapi_server/database
openapi_server/test/test_default_controller.py
```