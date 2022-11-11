
# Time Server on Raspberry Pi with Nodejs 
Implement time server with Nodejs and run on Raspberry Pi.

Google Slide Link:
https://docs.google.com/presentation/d/1obf5JwOFBl9sIlIrdM0Ci7tMdmmW_jZ2s8rWBh3FA8w/edit?usp=sharing


## TCP time server
Your server should listen to TCP connections on the port provided by the first argument to your program. For each connection you must write the current date & 24 hour time in the format: "YYYY-MM-DD hh:mm"
## HTTP server 
that serves JSON data when it receives a GET request to the path '/api/parsetime'. Expect the request to contain a query string with a key 'iso' and an ISO-format time as the value.
## Design
### TCP Server 
Step 1: on the server side


$ node time_server.js 8000


Step 2: On the client side browser


http://localhost:8000/

### HTTP Server 
Step 1: On the server


$ node http_json_api_server.js 8000


Step 2: on the client browser


http://localhost:8000/api/parse_currenttime


Step 3: on the client browser


http://localhost:8000/api/unix_currenttime

## Implementation 
### Code Source
time-server.js


time-server-parse-time.js

## Test
Run the code on Raspberry Pi via VNC Viwer platform.
