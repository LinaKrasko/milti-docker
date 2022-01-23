# Specify a base image
FROM node:16-alpine

# Install some dependencies
WORKDIR /app
COPY ./package.json ./

RUN npm install
COPY . .

# Default command
RUN npm run builds

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html

