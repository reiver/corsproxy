# corsproxy

This is a proxy HTTP server that adds permissive **cross-origin resource sharing** (**CORS**) headers to the response.

For example, if the following URL didn't have CORS headers:
```
http://example.com/user/joeblow.atom
```

Then, if the `corsproxy` serving on the Internet domain `corsproxy.tld`, then the following would give the return the same data with permissive CORS headers added:
```
http://corsproxy.tld/http://example.com/user/joeblow.atom
```

## CORS Headers

The CORS headers that are added are:
```
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET, DELETE, HEAD, OPTIONS, PATCH, POST, PUT, TRACE
```

## Author

Software **corsproxy** was written by [Charles Iliya Krempeaux](http://reiver.link)
