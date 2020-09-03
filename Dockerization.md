#Dockerization

##Angular
Two Steps
1. Build step
2. Run 

###Sample image
```json
### STAGE 1: Build ###
FROM node:12.7-alpine AS build
WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build

### STAGE 2: Run ###
FROM nginx:1.17.1-alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build /usr/src/app/dist/aston-villa-app /usr/share/nginx/html
```

###Selecting Base Image

[Choose Base Image](https://derickbailey.com/2017/03/09/selecting-a-node-js-image-for-docker/)
1. NodeJs version
2. Debian or Alpine
3. Full, Slim or Alpine
