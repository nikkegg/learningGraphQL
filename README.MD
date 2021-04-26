# Why choose GraphQL over REST

Typical API is built using REST principles, which means the following in practice:
1. (Multiple) fixed endpoints returning predetermined data, e.g
myapi.org/users

    myapi.org/user/id

2. REST APIs are stateless, meaning that requests can be made independently of one another, and each crequest contains all of the data necessary to complete itself successfully.

3. Assumes independence between server and the client

4. RESt APIs structure data in an intuitive one-to-one map fashion - one endpoint returns one given type of response (e.g myapi.org/users cannot (or more to the point should not) return data from myapi.org/products)
5. As a negative consequence of point above, REST APIs are pront to under and overfetching.
    1. Underfetching -

On the other hand GraphQL is a new API standard developed and open-sourced by Facebook. It supports declarative data fetching, where the client can specifies exactly (by sending a POST request) what data it needs to retreive from the API.
GraphQL is often confused with being a database technology. This is a misconception - GraphQL is a query language for *APIs*, not databases. In that sense it’s database agnostic and effectively can be used in any context where an API is used and GraphQL is configured.


GraphQL differs from rest in the following ways:

1. Instead of multiple endpoints that return fixed data structures, a GraphQL server only exposes a single endpoint and responds with precisely the data a client asked for.
2.
