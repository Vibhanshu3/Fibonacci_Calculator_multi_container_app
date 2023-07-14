from node:14-alpine

WORKDIR '/app'

copy package.json .

run npm install

copy . .

cmd ["npm", "run", "start"]