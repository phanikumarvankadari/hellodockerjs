# hellodocker
1. docker pull node:latest
2. create a file named Dockerfile and add the following code
# Use the official Node.js image from the Docker Hub
FROM node:latest

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the application will run on
EXPOSE 3000

# Define the command to run the application
CMD ["node", "app.js"]


3. on command line npm init -y creates a package.json
4. make /import sample node js project which you want to deploy using a docker
5. sample app.js is below
6. build docker with 'docker build -t my-node-app .' on terminal
7. start app with 'docker run -p 3000:3000 my-node-app' on terminal.




