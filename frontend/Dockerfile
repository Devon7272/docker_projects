# In this dockerfile we are going to build a production grade environment for our nodejs app this will outline a multi-step build process that will show us how a production environment should look. We don't need to the volumes setup anymore here now that this is a production environment, we used the volumes so that we can see our immediate changes show up inside our containers. 

# This is our build phase
FROM node:16-alpine as builder

WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build 

# This is our run phase
FROM nginx 
COPY --from=builder /app/build /usr/share/nginx/html

# docker build . 
# docker run -p 8080:80 (default port for nginx is 80)