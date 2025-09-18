### Deployment in Github Pages

1. `git branch gh-pages` (only need to do this the first time you deploy)
2. Commit all work
3. `git checkout gh-pages && git merge main --no-edit`
4. `npm run build` (check scripts)
5. `git add dist -f && git commit -m "Deployment commit`
6. `npm run deploy` (check scripts)
7. `git checkout main`

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

### Linting & Formatting

I haven't set up the project with these yet, so manually install and configure them if you want.

#### ESLint

- To install it, refer to the [docs](https://eslint.org/docs/latest/use/getting-started).
- You can use the default config, or use other configs (like `eslint-config-airbnb`).
- Running `npx eslint` finds linting errors and `npx eslint --fix` fixes them.
- Enable the extension in VSC.

#### Standard

- This is an alternative to ESLint, it automatically comes pre-configured with ESLint rules to match the javascript standard style.
- Install it using `npm install -D standard`.
- To use it, run `npx standard` to find errors and `npx standard --fix` to fix them.

#### Prettier

- Refer to the [official website](https://prettier.io/).
- You can use the default config or a custom config.
- Enable the extension in VSC.
