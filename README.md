# ResponseCachingDemo

This solution demonstrates how to use ResponseCaching Middleware in DotNet Core.

In ASP.NET Core, the Response Caching Middleware is a middleware component that allows you to cache the HTTP responses
returned by your application. Caching responses can significantly improve the performance and scalability of your web
application by reducing the processing and data transfer overhead.

The Response Caching Middleware intercepts incoming requests and checks if there is a cached response available for that request.
If a valid cached response is found, it is directly returned to the client without invoking the entire request pipeline.
This saves processing time and reduces the load on your application.

When a request arrives at the Response Caching Middleware, it examines the request headers to determine if it can be cached.
The middleware uses the Cache-Control headers to determine the caching behavior. If the request is cacheable,
the middleware checks if a cached response exists for the given request. If a cached response is found and it is still valid,
the middleware returns it directly. If a valid cached response does not exist, the middleware allows the request to proceed through
the pipeline and then caches the response before sending it back to the client.

By adding the AddResponseCaching method to the service collection and using the UseResponseCaching method in the request pipeline,
you enable the Response Caching Middleware in your application.
