# HTTP

### GET request limit?

Get request itself doesn’t have limit but the web-server and the browsers have configurable limit. But it’s 8K in webserver



### HTTPS verbs

1. GET: retrieve data
2. POST: insert data
3. PUT: Update and replace data
4. PATCH: update and modify data
5. Delete: delete data
6. HEAD: It doesn't have body, and mostly using before loading a large resource to check the size, last modification, etc.

### HTTP headers:

let the client and the server pass additional information with an HTTP request or response. An HTTP header consists of its **case-insensitive** name followed by a colon \(:\), then by its value. Whitespace before the value is ignored.

#### Request headers

Cookie, Host, Referrer, User-Agent, Accept \(what kind of MIME types it can accept in response\), Authentication\(Basic: base64 of user/pass, Bearer: JWT, OAUTH 2.0\)

#### Response headers

Content-Type, Access-Control-Allow-Origin, Content-Encoding







