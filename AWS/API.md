# REST API: 
REST (Representational State Transfer) is an architectural style for designing networked applications. It provides a set of guidelines and principles for creating scalable and reliable web services. REST APIs are the implementations of these principles, allowing systems to communicate with each other over the internet.

Here are some key characteristics of REST APIs:

1. Stateless: REST APIs are stateless, meaning that each request from a client to the server should contain all the necessary information for the server to understand and process the request. The server does not retain any information about the client's previous requests.

2. Resource-based: REST APIs model the application's functionality as a set of resources, which can be objects, data, or services. Each resource is identified by a unique URL (Uniform Resource Locator), and clients interact with these resources by sending HTTP requests.

3. CRUD Operations: REST APIs typically support the four fundamental operations on resources: Create, Read, Update, and Delete (CRUD). HTTP methods such as GET, POST, PUT, PATCH, and DELETE are used to perform these operations on the corresponding resources.

4. Uniform Interface: REST APIs follow a uniform interface, which means they use standard HTTP methods, status codes, and headers for communication. This allows for a consistent and predictable interaction between clients and servers.

5. Hypermedia as the Engine of Application State (HATEOAS): HATEOAS is a principle in REST that suggests including hyperlinks in API responses, allowing clients to discover and navigate related resources. These hyperlinks provide the necessary information for clients to transition between different application states.

6. Representation-oriented: REST APIs use different representations (such as JSON, XML, or HTML) to represent resources in the request and response payloads. The client and server negotiate the format of the representations using the "Content-Type" header.

7. Stateless Server: The server does not maintain any client session state. Each request from the client should be self-contained, and the server responds based solely on the information provided in the request.

8. Scalability and Caching: REST APIs can take advantage of caching mechanisms to improve performance. The server can specify caching instructions using HTTP headers, allowing clients to cache responses and reduce the load on the server.

# GraphQL
- GraphQL is an open source server-side technology which was developed by Facebook to optimize RESTful API calls. It is an execution engine and a data query language.

Turotial: https://www.tutorialspoint.com/graphql/graphql_architecture.htm

## Server Essentials & Description
1. Schema
- A GraphQL schema is at the center of any GraphQL server implementation and describes the functionality available to the clients which connect to it.
2. Query
- A GraphQL query is the client application request to retrieve data from database or legacy API's.
3. Resolver
- Resolvers provide the instructions for turning a GraphQL operation into data. They resolve the query to data by defining resolver functions.

4. Types:
- https://www.tutorialspoint.com/graphql/graphql_type_system.htm