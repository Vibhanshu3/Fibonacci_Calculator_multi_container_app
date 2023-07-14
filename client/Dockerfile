from node:14-alpine as builder

WORKDIR '/app'

copy package.json .

run npm install

copy . .

run npm run build

from nginx
EXPOSE 3000
copy ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html