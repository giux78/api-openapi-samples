# openapi-samples
API samples following given specs.

## Converting swagger to openapi-v3

Just use this online API

        https://mermade.org.uk/api/v1/convert?url=$YOUR_URL

eg.

        https://mermade.org.uk/api/v1/convert?url=https://sgiauth.azurewebsites.net/explorer/swagger.json

## Converting openapi-v3 to openapi-v2

To convert between formats use:

        ./bin/api-spec-converter.sh $INFILE -f openapi_3 -t swagger_2 -s yaml  > $OUTFILE

To convert all v3 files to v2, use:

        find openapi-v3/ -name \*.yaml \
          -exec bash -c 'I="{}"; ./bin/api-spec-converter.sh "$I" -f openapi_3 -t swagger_2 -s yaml > "${I//v3/v2}" ' \;


## Generating JSONSchema from existing json

See https://github.com/perenecabuto/json_schema_generator


## API Tools

  - SwaggerHub OpenAPI v3, v2 editor https://editor.swagger.io
  - OpenAPI v3, v2 editor by Red Hat https://github.com/apicurio/apicurio-studio

