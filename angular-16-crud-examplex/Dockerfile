# Use an official Node.js runtime as a base image
# FROM node:20-alpine

# # Set the working directory in the container
# WORKDIR /usr/src/app

# # Copy package.json and package-lock.json to the container
# COPY package*.json ./

# # Install dependencies
# RUN npm install

# # Copy the rest of the application files to the container
# COPY . .

# # Expose the port the app runs on
# EXPOSE 4200

# # Start the application
# CMD ["npm", "start"]
FROM node:slim
WORKDIR /app
RUN npm install -g @angular/cli
COPY package.json package-lock.json ./
RUN npm install
COPY . .
EXPOSE 4200
CMD ["ng", "serve", "--host", "0.0.0.0","--disable-host-check"]