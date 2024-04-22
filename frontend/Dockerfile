# Telling Docker to use the node:17-alpine image as the base image for the container.
FROM node:20.11.1-alpine

# Create a directory and go to the directory
WORKDIR /app

# Copy the package.json file to my current directory to install the necessary dependence
COPY package.json .

# Install the dependence
RUN npm install

# Copy other files to my current directory
COPY . .

# Open the port to react
EXPOSE 5173

# Layer 7: Telling Docker to run the `npm start` command when the container is started.
CMD ["npm", "run", "dev"]