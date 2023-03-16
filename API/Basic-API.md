# Common API Attributes and Methods
The VTK.js API is quite systematic in its use of attributes and methods. Rather than explaining these attributes and methods repeatedly throughout the glossary we'll tackle them here generally and note only differences in the individual glossary entries.

## newInstance()
This method is used to create a new instance of a class, for example, one might use `newInstance()` to define a object instance of a render window like so:
```js
const renderWindow = vtkRenderWindow.newInstance();
```

# vtkFullScreenRenderWindow
- `.newInstance()`
- `.getRenderer()`
- `.getRenderWindow()`

Resources:
- https://kitware.github.io/vtk-js/api/Rendering_Misc_FullScreenRenderWindow.html

# vtkActor
Represents an entity in a rendering scene.
- `.newInstance()`
- `.setMapper()`
- "The `vtkActor` is used to hold position, orientation and scaling information about the data, as well as a pointer to both the property and the mapper."[^1]

Resources:
- https://kitware.github.io/vtk-js/api/Rendering_Core_Actor.html

# vtkMapper
An abstract class that is used to define the interface between the data and the graphics primitives.
- `.newInstance()`
- `.setInputConnection()`
- "the `vtkMapper` subclass is ressponsible for actually rendering the data."[^1]

Resources:
- https://kitware.github.io/vtk-js/api/Rendering_Core_Mapper.html

# vtkConeSource
Creates a cone with specified properties.
- `.newInstance()`
- `.getOutputPort()`

Resources:
- https://kitware.github.io/vtk-js/api/Filters_Sources_ConeSource.html

# vtkProperty
- "The `vtkProperty` object captures various parameters that control the appearance of the data such as the ambient lighting coefficient and whether the object is flat, Gouraud, or Phong shaded."[^1]

# vtkRenderer
A viewport that holds the actor, cameras, lights, etc.
- `.addActor()`
- `.resetCamera()`

Resources:
- https://kitware.github.io/vtk-js/api/Rendering_Core_Renderer.html

# vtkRenderWindow
- An abstract object used to define a specific rendering window.
- The rendering window is the location where the final image is displayed (as created by the renderer).
- `.render()`

Resources:
- https://kitware.github.io/vtk-js/api/Rendering_Core_RenderWindow.html





# Footnotes
- [^1]: VTK User Guide, Chapter 7 Volume Rendering, pp. 139-140.