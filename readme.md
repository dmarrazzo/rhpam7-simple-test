Simple Test for RHPAM 7.0.2
===========================

Deploy the project.

API examples:

### Start the process

curl -u user:password -X POST "http://localhost:8080/kie-server/services/rest/server/containers/simple-test_1.0.0/processes/src.simple-test-proc/instances" -H "accept: application/json" -H "content-type: application/json" -d "{}"

### List the process instances

curl -u user:password -X GET "http://localhost:8080/kie-server/services/rest/server/containers/simple-test_1.0.0/processes/instances" -H "accept: application/json"

### Send a signal

curl -u user:password -X POST "http://localhost:8080/kie-server/services/rest/server/containers/simple-test_1.0.0/processes/instances/signal/signal?instanceId=2" -H "accept: application/json" -H "content-type: application/json" -d "{}"

### Abort the process

curl -u user:password -X DELETE "http://localhost:8080/kie-server/services/rest/server/containers/simple-test_1.0.0/processes/instances/2" -H "accept: application/json"
