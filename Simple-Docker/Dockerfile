# Specify Base Image
FROM node:alpine

WORKDIR /usr/app

# Install Dependencies
COPY ./package.json ./
RUN npm Install
COPY ./ ./

# Default Command
CMD ["npm", "start"]