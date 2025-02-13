# http-status-string

A simple and lightweight NPM package that provides HTTP status codes as easily readable string keys. Instead of remembering numeric HTTP status codes, developers can use intuitive key names like `CONTINUE_100`, `OK_200`, `NOT_FOUND_404`, and `INTERNAL_SERVER_ERROR_500` to improve code readability and maintainability.

## Installation

Install the package via npm:

```sh
npm install http-status-string
```

or using yarn:

```sh
yarn add http-status-string
```

## Usage

Import and use the package in your project:

```javascript
const { HttpStatus } = require('http-status-string');

console.log(HttpStatus.OK_200); // 200
console.log(HttpStatus.NOT_FOUND_404); // 404
console.log(HttpStatus.INTERNAL_SERVER_ERROR_500); // 500
```

## HTTP Status Codes

### 1xx: Informational Responses

| Status Code | Name                           | Description                                                  |
|------------|--------------------------------|--------------------------------------------------------------|
| 100        | CONTINUE_100                   | The request has been received and the process is continuing. |
| 101        | SWITCHING_PROTOCOLS_101        | The server is switching protocols as requested.              |
| 102        | PROCESSING_102                 | The request is being processed but no response is available yet. |
| 103        | EARLY_HINTS_103                | The server is sending hints before the final response.       |

### 2xx: Success Responses

| Status Code | Name                           | Description                                                  |
|------------|--------------------------------|--------------------------------------------------------------|
| 200        | OK_200                         | The request was successful.                                  |
| 201        | CREATED_201                    | The request was successful, and a new resource was created.  |
| 202        | ACCEPTED_202                   | The request has been accepted for processing but is not completed. |
| 203        | NON_AUTHORITATIVE_INFORMATION_203 | The request was successful but may be from another source. |
| 204        | NO_CONTENT_204                 | The request was successful, but there is no content to return. |
| 205        | RESET_CONTENT_205              | The request was successful, and the client should reset the document view. |
| 206        | PARTIAL_CONTENT_206            | The server is delivering only part of the resource due to a range header sent by the client. |
| 208        | ALREADY_REPORTED_208           | The resource was already reported earlier. |
| 226        | IM_USED_226                    | The server has completed a GET request using instance manipulations. |

### 3xx: Redirection Responses

| Status Code | Name                           | Description                                                  |
|------------|--------------------------------|--------------------------------------------------------------|
| 300        | MULTIPLE_CHOICES_300           | The requested resource has multiple choices.                 |
| 301        | MOVED_PERMANENTLY_301          | The requested resource has moved permanently.                |
| 302        | FOUND_302                      | The requested resource is found but temporarily moved.       |
| 303        | SEE_OTHER_303                  | The response can be found at another URI using a GET method. |
| 304        | NOT_MODIFIED_304               | The resource has not been modified since the last request.   |
| 307        | TEMPORARY_REDIRECT_307         | The request should be repeated at another URI.              |
| 308        | PERMANENT_REDIRECT_308         | The request should be repeated at another URI permanently.  |

### 4xx: Client Errors

| Status Code | Name                           | Description                                                  |
|------------|--------------------------------|--------------------------------------------------------------|
| 400        | BAD_REQUEST_400                | The request could not be understood due to malformed syntax. |
| 401        | UNAUTHORIZED_401               | Authentication is required to access this resource.         |
| 402        | PAYMENT_REQUIRED_402           | Payment is required to access this resource.               |
| 403        | FORBIDDEN_403                  | The server understands the request but refuses to authorize it. |
| 404        | NOT_FOUND_404                  | The requested resource could not be found.                   |
| 405        | METHOD_NOT_ALLOWED_405         | The request method is not supported for the resource.       |
| 406        | NOT_ACCEPTABLE_406             | The requested resource is not acceptable according to headers. |
| 408        | REQUEST_TIMEOUT_408            | The server timed out waiting for the request.              |
| 409        | CONFLICT_409                   | The request conflicts with the current state of the resource. |
| 410        | GONE_410                       | The resource is no longer available and has been removed.  |
| 411        | LENGTH_REQUIRED_411            | The request requires a valid Content-Length header. |
| 412        | PRECONDITION_FAILED_412        | The request failed precondition checks. |
| 413        | PAYLOAD_TOO_LARGE_413          | The request payload is too large. |
| 414        | URI_TOO_LONG_414               | The requested URI is too long. |
| 415        | UNSUPPORTED_MEDIA_TYPE_415     | The media type of the request is unsupported. |
| 416        | RANGE_NOT_SATISFIABLE_416      | The requested range is invalid. |
| 417        | EXPECTATION_FAILED_417         | The expectation in the request headers could not be met. |
| 429        | TOO_MANY_REQUESTS_429          | The user has sent too many requests in a given time.       |

### 5xx: Server Errors

| Status Code | Name                           | Description                                                  |
|------------|--------------------------------|--------------------------------------------------------------|
| 500        | INTERNAL_SERVER_ERROR_500      | The server encountered an unexpected condition.             |
| 501        | NOT_IMPLEMENTED_501            | The request method is not supported by the server.         |
| 502        | BAD_GATEWAY_502                | The server received an invalid response from an upstream server. |
| 503        | SERVICE_UNAVAILABLE_503        | The server is temporarily unable to handle the request.    |
| 504        | GATEWAY_TIMEOUT_504            | The server did not receive a timely response from an upstream server. |
| 505        | HTTP_VERSION_NOT_SUPPORTED_505 | The HTTP version used in the request is not supported.     |
| 508        | LOOP_DETECTED_508              | The server detected an infinite loop while processing the request. |

## Non-Major Status Codes
These status codes are used less frequently but still hold importance in specific scenarios.

| Status Code | Name                            | Description                                               |
|------------|---------------------------------|-----------------------------------------------------------|
| 418        | IM_A_TEAPOT_418                 | The server refuses to brew coffee because it is a teapot. |
| 422        | UNPROCESSABLE_ENTITY_422        | The request was well-formed but could not be processed.  |
| 451        | UNAVAILABLE_FOR_LEGAL_REASONS_451 | The resource is unavailable due to legal reasons.       |

## About the Author

This package is developed and maintained by **Seiam Al Mahmud**. He is a passionate web developer experienced in JavaScript, Node.js, React, and backend technologies. You can find more about his work on his GitHub profile:

[GitHub: SeiamAlMahmud](https://github.com/SeiamAlMahmud)

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License.

