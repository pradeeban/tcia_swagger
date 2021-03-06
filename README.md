# TCIA Swagger API Definitions

TCIA Swagger API definitions were created by using the Swagger Inspector and SwaggerHub.

The steps followed:

Run the REST end point in Swagger Inspector.

Create Open API Definition by "Go to SwaggerHub" and Import OpenAPI.

Now, export to YAML from the SwaggerHub.

Update the auto-generated YAML with the relevant service descriptions.

Deploy the API definitions in your Swagger-UI local installations.

Currently we run Swagger with Docker:

$ docker run -p 80:8080 -e "SWAGGER_JSON=/tcia.json" -v /home/ex-pradeebankathira/tcia.json:/tcia.json swaggerapi/swagger-ui &


It appears that it is not possible to pass a YAML file at startup time to open the Swagger API with that.

Therefore, we open the final YAML file with SwaggerHub and export it as JSON to start our Swagger instance with the JSON file.