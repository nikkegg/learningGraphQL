This repo is very high-level overview of GraphQL vs REST. It also icludes small Rails practice project with integrated GraphQL.
# Why choose GraphQL over REST

Typical API is built using REST principles, which means the following in practice:
1. (Multiple) fixed endpoints returning predetermined data, e.g
myapi.org/users

    myapi.org/user/id

2. REST APIs are stateless, meaning that requests can be made independently of one another, and each crequest contains all of the data necessary to complete itself successfully.

3. Assumes independence between server and the client

4. RESt APIs structures data in an intuitive one-to-one map fashion - one endpoint returns unique response (e.g myapi.org/users cannot (or more to the point should not) return data from myapi.org/products)
5. As a negative consequence of point above, REST APIs are prone to under and overfetching.
    1. Underfetching -
    2. Overfetching - imagine that I want to only fetch 3 top users (by any metric for "top" - number of blog posts, number of purchases etc.). With REST APIs this is impossible - normally I would have to fetch all users, and then filter them out based on my needs. Alternative to this using REST, would be to specify separate endpoint which would return my top 3 users - but this would require creating separate endpoint for every metric. Also, what if I suddenly needed 5 top users? 10? Problem becomes apparent. Additionaly, if I want to feth users and, say their blog posts, normnally I would have to make two separate requests, such as myapi.org/users and myapi.org/user/id/blog_posts for each of the users, resulting in *N+1 query* problem. Not very efficient, especially if we think about mobile devices.

On the other hand GraphQL is a new API standard developed and open-sourced by Facebook. It supports declarative data fetching, where the client can specifies exactly (by sending a POST request) what data it needs to retreive from the API.
GraphQL is often confused with being a database technology. This is a misconception - GraphQL is a query language for *APIs*, not databases. In that sense it’s database agnostic and effectively can be used in any context where an API is used and GraphQL is configured.


GraphQL differs from REST in the following ways:

1. Instead of multiple endpoints that return fixed data structures, a GraphQL server only exposes a single endpoint and responds with precisely the data a client asked for.
2. Scales flexibly
3. Solves under and overfetching problem.

