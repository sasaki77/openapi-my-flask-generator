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

## Edit `.openapi-generator-ignore`

Edit `.openapi-generator-ignore' to prevent some files from being overwritten.

```
openapi_server/test
.git_push.sh
openapi_server/database
```