# Use existing docker image as base, creates a temp image id and snapshot 
FROM alpine

# Download and install a dependency created a temp image id and snapshot in a temp container
RUN apk add --update gcc
RUN apk add --update redis

# Tell the image what to do when it starts as a container, this step gets its third image id to prep for the final id that we will use
CMD ["redis-server"]