# Use NodeJS base image
FROM node:alpine

# Create app directory
WORKDIR /app

# Copy package.json and package-lock.json to app directory
COPY package*.json ./

# Install dependencies
RUN npm install 

# Install typescript globally to able build source code
RUN npm install -g typescript

# Copy source code to app directory
COPY . .

# Build the source code
RUN npm run build

# Bind the port that the image will run on
EXPOSE 8080

# Define the Docker image's behavior at runtime
CMD ["node", "www/server.js"]
