# api_examples


## APIs

Application programming interfaces are a communication layer that provides the
interface for two software applications.

The model for APIs is usually referred to as request and reponse. This is also known as calling an API

### Web APIs 

*Design Model Basics*

The longstanding models for querying APIs on the web are SOAP and REST.
Simple Object Access Protocol (SOAP) typically deals with XML documents strictly.
Representational State Transfer (REST) is more closely related to HTML and HTTP.
There are other models and languages for querying APIs includinh GraphQL.

*Consuming Web APIs*

Calls to the APIs URL, are made using a base url and its endpoints as resources.
The API Reference usually discloses these.  
It is best to use https:// URLs whenever possible for security.

Requests are pieced together with the base URL, endpoint, method, etc.
Responses are returned by the server and contain data/content and status code.
Headers are included in all requests and responses.
HTTP Methods: POST, GET, PUT, PATCH
Response codes: 2xx, 3xx, 4xx, 5xx
see [Response Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)


**In Python:**

Start by installing the requests library in pip
$ python -m pip install requests

The basic invocation can be made with requests.get(url)
This object can be assigned to the API response, response = requests.get(url)
with attributes:
  * response.text
  * response.status_code
  * response.headers
  * response.request


The attribute for the request can also be assigned, request = response.request
with attributes:
  * attributes request.url
  * request.path_url
  * request.method
  * request.headers