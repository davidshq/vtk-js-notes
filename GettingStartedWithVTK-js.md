# Initialize a new project
1. `mkdir my-vtkjs-app`
2. `cd my-vtkjs-app`
3. `npm init`
4. `npm i @kitware/vtk.js`
5. `npm i -D webpack-cli webpack webpack-dev-server`
6. `mkdir dist/ src/`

# Add the static index.html file
Create an `index.html` file in the `dist` subdirectory with the following contents:

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
  </head>
  <body>
    <script src="./main.js"></script>
  </body>
</html>
```

# Update the scripts section
Edit the `scripts` section of the project's `package.json` so it looks like this:
```json
"scripts": {
    "build": "webpack --progress --mode=development",
    "start": "webpack serve --progress --mode=development --static=dist",
    "test": "echo \"Error: no test specified\" && exit 1"
},
```

# Creating hello world project
Create an `index.js` file in the `src` subdirectory with the following contents:
```js
import @kitware/vtk.js/Rendering/Profiles/Geometry;

import vtkFullScreenRenderWindow from '@kitware/vtk.js/Rendering/Misc/FullScreenRenderWindow';
import vtkActor from '@kitware/vtk.js/Rendering/Core/Actor';
import vtkMapper from '@kitware/vtk.js/Rendering/Core/Mapper';
import vtkConeSource from '@kitware/ctk.js/Filters/Sources/ConeSource';

const fullScreenRenderer = vtkFullScreenRenderWindow.newInstance();
const renderer = fullScreenRenderer.getRenderer();
const renderWindow = fullScreenRenderer.getRenderWindow();

// Create the cone
const coneSource = vtkConeSource.newInstance({ height: 1.0 });

const mapper = vtkMapper.newInstance();
mapper.setInputConnection(coneSource.getOutputPort());

const actor = vtkActor.newInstance();
actor.setMapper(mapper);

renderer.addActor(actor);
renderer.resetCamera();
renderWindow.render();
```

# Run the project
1. `npm run start`
2. Open a browser and navigate to `http://localhost:8080/`

# Resources
The above is a slightly simplified / streamlined version of the [Starting a vtk.js project from scratch](https://kitware.github.io/vtk-js/docs/vtk_vanilla.html) documentation.