# What is NGINX?
NGINX is Web Server written in C that can also act as a reverse Proxy Server, Gateway, Load Blancer and more.

# Versions
1. NGINX Opensource -> NGINX.org
2. NGINX Plus -> NGINX.com

# Getting Started

## Basic Server
Serves static pages from the specified root path.

```javascript
http{ // Block Directive
  server{ //Block Directive
    listen 8080; //Listen on port 8080 | Directive
    root <path>; //Path to be served
    }
}

events{}
```

## Terminology
1. Block Directives -> houses other directives inside it
2. Directives

## Location Directive

```javascript
http{
    server{
        listen 8080;
        root C:\abc\apps\html;

        location /images {
            root "H:/My Documents/My Pictures/"; // Note: quotes if you have space in your path
        }
    }
}

events{}
```

## Simple Load Balancer (Uses Round Robin)
```javscript
http{
    upstream backend{
    #ip_hash; // Use for sticky session based on ip address | default is round robin
    server 127.0.0.1:2222;
    server 127.0.0.1:3333;
    server 127.0.0.1:4444;
    }
    server{
        listen 80;
        
        location / {
        proxy_pass http://backend/
        }
        
    }
}

events{}
```

## Simple gRPC Server
```
http {
    log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
                      '$status $body_bytes_sent "$http_referer" '
                      '"$http_user_agent"';
 
    server {
        listen 80 http2;
 
        access_log logs/access.log main;
 
        location / {
            # Replace localhost:50051 with the address and port of your gRPC server
            # The 'grpc://' prefix is optional; unencrypted gRPC is the default
            grpc_pass grpc://localhost:50051;
        }
    }
}
```

