# Search UI

![image](https://github.com/user-attachments/assets/7daeeb74-df61-4028-8d59-a0e050cf5096)

## To Do Items:
- Add animation to logo when a "search query" is sent. The animation could be a multi-revolution rotation, or a jostle.
- To facilitate the animation being seen, add a delay from the transition of the search page to the result page.
- Add mock data for "results" returned when a search is done. This is to populate 'X' or 'N' result cards from an API response, instead of hardcoding that many.
- Implement an internal state and store system, either through the newly supported Pinia or the legacy Vuex.

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
