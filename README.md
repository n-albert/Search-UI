# Search UI

![image](https://github.com/user-attachments/assets/7daeeb74-df61-4028-8d59-a0e050cf5096)

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### If using Dockerfile + Docker

```sh
docker build -t vuejs-cookbook/dockerize-vuejs-app .

docker run -it -p 8080:80 --rm --name dockerize-vuejs-app-1 vuejs-cookbook/dockerize-vuejs-app
```
