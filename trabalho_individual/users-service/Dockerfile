FROM node:14

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package.json /app
COPY yarn.lock /app

RUN yarn

# Bundle app source
COPY . /app

EXPOSE 7101
CMD yarn db:migrate && yarn watch