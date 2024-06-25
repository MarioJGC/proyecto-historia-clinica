from node:20-alpine as  build-step

RUN mkdir -p /app

WORKDIR /app

copy package.json /app

run npm install

copy . /app

run npm run build --prod

from nginx:1.24.0-alpine

copy --from=build-step /app/dist/Pokeapp /usr/share/nginx/html