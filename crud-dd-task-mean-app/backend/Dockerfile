# Use the official Node.js 18 image as the base
FROM node:18

# Create and set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies first
# This helps with Docker caching for faster subsequent builds
COPY package*.json ./

# Install the backend dependencies
RUN npm install

# Copy the rest of your backend source code into the container
COPY . .

# Expose the port your Express/Node app runs on (usually 3000)
EXPOSE 3000

# The command to start your application
CMD ["npm", "start"]