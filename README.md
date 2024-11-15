# nginx-notes
Notes for NGINX

Used 

# 2 Different use case
- Web Server
- Reverse Proxy

# NGINX as Web Server
Just like other web servers, NGINX handles requests from browsers and serves them the web pages they ask for. But it does this with exceptional speed, especially when dealing with static content like images, videos, and plain HTML files.
- Basically this is where your app will run nothing else. It will serve your application.

# NGINX as Proxy Server
NGINX can sit in front of your web servers, acting as a middleman between the outside world and your servers. It’s like a gatekeeper that decides which server should handle each request, helping to balance the load and protect your servers from direct exposure to the internet.
- Security: expose only one entrypoint thus preventing hackers from accessing your server independently reducing your attack surface.
- Caching: Cache static files like images, html, etc... instead of calling your app for every request.
- Load balance: Load balance the request in different instances of your app making your app resilience.
- Compression: Reducing bandwidth usages
- Segmentation: For files instead of sending the whole file at once it will send in chunks only providing what you need part of the file best use in videos and music
- SSL encryption: Provide your app HTTPS connections only.

### NGINX CONFIG ###

## Context
- Is the high level enclosing tags {}
### Top level context
  - events
  - http
  - mail
  - stream

## Block
- is the enclosing tags {} inside the context. Basically the children of context.
### Common blocks
  - server
  - upstream

## Directives
- Is the key value pairs

# Useful Links
https://medium.com/@nomannayeem/mastering-nginx-a-beginner-friendly-guide-to-building-a-fast-secure-and-scalable-web-server-cb075b423298
https://gitlab.com/twn-youtube/nginx-crash-course/-/blob/main/nginx.conf?ref_type=heads