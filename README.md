### Angular App optimized

Based on [Angular Tour Of Heroes](https://angular.io/guide/universal)
### How to build

```
# Docker config for nginx with gzip compression
docker run -d --name web-server --network=host nginx:1.17.3-alpine
docker cp nginx.conf web-server:/etc/nginx/nginx.conf
docker exec -ti web-server nginx -s reload

# Build and run the SSR app
yarn
yarn build:ssr && yarn serve:ssr
```