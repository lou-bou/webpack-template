### Deployment in Github Pages
1) `git branch gh-pages` (only need to do this the first time you deploy)
2) Commit all work
3) `git checkout gh-pages && git merge main --no-edit`
4) `npm run build` (check scripts)
5) `git add dist -f && git commit -m "Deployment commit`
6) `npm run deploy` (check scripts)
7) `git checkout main`

### Starting a server
Run: `npm run dev`

### Linking CSS
Put this in `index.js`:
```js
import "./[filename].css";
```

### Using images in Javascript
Put this in `index.js`:
```js
import odinImage from "./odin.png";
   
// select image element

image.src = odinImage;
```

### Adding dependencies
- Add dev dependencies to `webpack.dev.js`
- Add prod dependencies to `webpack.prod.js`
- Add dependencies that both modes need to `webpack.common.js`