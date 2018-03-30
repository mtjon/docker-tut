# Always be specifc in your images - especially in production - Docker will use the `:latest` tag by default.
# Failing to do so may result in unexpected dependecy issues or new/ deprecated functions.
FROM nginx:1.13.10

# Use label to add metadate to your image.
LABEL maintainer='You name <email>'

# Set the working directory within the image
WORKDIR /usr/share/nginx/html

# Copy a file from host to image
# as nginx is a webserver, let's copy a simple index.html
COPY index.html index.html

# EXPOSE and CMD are already definded in the FROM image and do not need to be specified.
# Usually you need to define an entrypoint for the image, as the container runs as a process.