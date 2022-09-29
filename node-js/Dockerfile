# Specify image need to specify node for the alpine image
FROM node:alpine

# Install same dependencies, after npm version 15 nodejs needs a WORKDIR to build successfully 
WORKDIR /usr/app
# This is to minimize cache busting and rebuilds 
COPY ./package.json /usr/app/
RUN npm install 
COPY ./ ./

# Default command 
CMD ["npm", "start"]