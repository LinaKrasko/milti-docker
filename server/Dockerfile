# Specify a base image
FROM node:14.14.0-alpine

# Install some dependencies
WORKDIR /app
COPY ./package.json ./

RUN npm install
COPY . .

# Default command
CMD ["npm", "run", "start"]
