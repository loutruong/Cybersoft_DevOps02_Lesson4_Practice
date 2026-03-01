# Pull application / software image of node.js from hub.docker.com
FROM node:latest

# Set the working directory
WORKDIR /nodejs

# Copy the package.json and yarn.lock files
COPY package*.json ./

# Set the network timeout to a higher value (in milliseconds) to prevent timeouts during installation
RUN yarn config set network-timeout 3000000
# Install the application dependencies
RUN yarn install

# Copy the source code files in same level with Dockerfile to the working directory
COPY . .

# Set the network timeout to a higher value (in milliseconds) to prevent timeouts during installation
RUN yarn config set network-timeout 3000000
# Install the application dependencies
RUN yarn install

# Expose port 8088 to the outside world
EXPOSE 8088

# Run the application when the container starts
CMD ["yarn", "start"]

# docker build . -t loutruongnode:1.0.0
# docker run -d -it --name node -p 8088:8088 loutruongnode:1.0.0
