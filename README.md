# NodeJS Express (server) with Angular CLI (client) Starter 
NodeJS Express (server) with Angular CLI (client) Starter 

## Development
```bash
$ npm run install:packages
$ npm run start
```

Browse the Client:
```bash
http://localhost:8080/
```

Browse the Server:
```bash
http://localhost:8080/api
http://localhost:8080/api/users
```

The `$ npm run start` execute the following script `concurrently --kill-others \"cd client && ng serve --disable-host-check --proxy-config proxy.conf.json\" \"cd server && nodemon ./bin/www\"`. Please have in mind the client/proxy.conf.json file.

```json
{
  "/api": {
    "target": "http://localhost:3000",
    "secure": false
  }
}
```
Please note that the PORT 3000 is the default NodeJS Express PORT.

## Build (dist)
```bash
$ npm run build
```

## Run Build
```bash
$ cd dist/server
$ PORT=8000 NODE_ENV=production node bin/www
```

Browse the Server:
```bash
http://localhost:8000/
http://localhost:8000/api
http://localhost:8000/api/users
```

## License

MIT © [George I. Tsopouridis](gtsopour@gmail.com)