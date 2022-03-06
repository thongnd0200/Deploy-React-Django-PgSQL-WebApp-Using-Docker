FROM node:14-alpine

WORKDIR /app
COPY package.json .
COPY package-lock.json .

RUN npm config get proxy
RUN npm config rm proxy
RUN npm config rm https-proxy
RUN npm install
COPY . .   
CMD ["npm", "start"]

