#select a base image
FROM node:20.11.1-alpine

RUN npm install -g nodemon

#create a directory and go to the directory
WORKDIR /app

#copy the package.json file to my current directory to install the necessary dependency
COPY package.json .

# Install the dependencies
RUN npm install

COPY . .

EXPOSE 5555

CMD ["npm", "run", "dev"]