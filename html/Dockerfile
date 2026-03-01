# Pull application / software image from hub.docker.com
FROM nginx:latest

# Set the nginx html directory
WORKDIR /usr/share/nginx/html

# Copy the source code files in same level with Dockerfile to the nginx html directory
COPY . .

# Expose port 80 to the outside world
EXPOSE 80

# docker build . -t loutruonghtml:1.0.0