FROM node:13.12.0-alpine

WORKDIR /user/src/app 

COPY ./package.json ./

COPY ./yarn.lock ./

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install app dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm install --silent

# add app
COPY . .

# start app
CMD ["npm", "start"]