# REST

### What does REST stand for?

 Representational State Transfer.

### What is an identifier of a resource? Give an example.

 A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

`https://adventure-works.com/orders/1`

### What are the most common HTTP verbs?

The most common operations are GET, POST, PUT, PATCH, and DELETE.

### What should the URIs be based on?

 On nouns (the resource) and not verbs (the operations on the resource).

### Give an example of a good URI.

`https://adventure-works.com/orders`

 Sending an HTTP GET request to the collection URI retrieves a list of items in the collection. Each item in the collection also has its own unique URI. An HTTP GET request to the item's URI returns the details of that item.


### What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

All web requests impose a load on the web server. The more requests, the bigger the load. Therefore, try to avoid "chatty" web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. Instead, you might want to denormalize the data and combine related information into bigger resources that can be retrieved with a single request. However, you need to balance this approach against the overhead of fetching data that the client doesn't need. Retrieving large objects can increase the latency of a request and incur additional bandwidth costs.

### What status code does a successful GET request return?

 A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

### What status code does an unsuccessful GET request return?

If the resource cannot be found, the method should return 404 (Not Found).

### What status code does a successful POST request return?

If a POST method creates a new resource, it returns HTTP status code 201 (Created). The URI of the new resource is included in the Location header of the response. The response body contains a representation of the resource.
If the method does some processing but does not create a new resource, the method can return HTTP status code 200 and include the result of the operation in the response body.

### What status code does a successful DELETE request return?

 The web server should respond with HTTP status code 204, indicating that the process has been successfully handled, but that the response body contains no further information.