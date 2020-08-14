# What is NGINX?
NGINX is Web Server that can also act as a reverse Proxy Server, Gateway, Load Blancer and more.

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
