# ManaGraph API

API REST service with endpoints for tracking basic data about MemGraph database instances.

## System requirements

In order to be able to run this app Node.js version greater or equal to 15.3.0 should be installed, since this app is written as an ES module and prior versions of Node had it as an experimental feature, therefore it is not officialy supported or tested on versions prior to 15.3.0.

## .env configuration

Configuration of this REST API service is possible via an .env file which should be put on the root folder of this project. These keys are supported:

1. EXPRESS_PORT - a numeric key which sets the port of the express app. In case of an invalid or missing value, port number 3000 will be used.
2. TEST_MEMGRAPH_INSTANCE_NAME - an arbitrary instance name used by unit tests. Default value for this parameter is "memgraph"
3. TEST_MEMGRAPH_INSTANCE_URI - should be an URI to a valid active memgraph instance used by unit tests. Default value for this parameter is "localhost:7687"
4. LOG_ALL_REQUESTS - a boolean flag which toggles loggin of all requests to the console. Default value is false
5. CONNECTION_TIMEOUT - an integer value in miliseconds representing connection timeout on neo4j driver. In case of an invalid or missing value, connection timeout will be set at 1000ms.
