# Cropping
- "Cropping is a method of defining visible regions of the structured volume using six planes—two along each of the major axes."[^3]
- "The six planes that are defined by the xmin, xmax, ymin, ymax, zmin, and zmax values break the volume into 27 regions (a 3x3 grid)."[^3]

# Color Transfer Function
- "maps the scalar value into a color."[^1]

# Data Array
- Keeps track of numerical values and their associated metadata (e.g. size, data type, etc.)

# Gradient Opacity Transfer Function
- "maps the magnitude of the gradient of the scalar value into an opacity multiplier."[^1]

# Scalar Opacity Transfer Function
- "maps the scalar value into an opacity or an opacity per unit length value."[^1]
- "For rendering techniques that map a pixel to a single location in the volume (such as an isosurface rendering or a maximum intensity projection) the ScalarOpacity transfer function maps the scalar value to an opacity."[^2]
- "When a compositing technique is used, the ScalarOpacity function maps
scalar value to an opacity that is accumulated per unit length for a homogenous region of that value."[^2]
- "The specific mapper then utilizes a form of compositing to accumulate the continuously changing color and opacity values through the volume to form a final color and opacity that is stored in the corresponding pixel."[^2]
- "The ScalarOpacity and Color transfer functions are typically used to perform a simple classification of the data. Scalar values that are part of the background, or that are considered noise, are mapped to an opacity of 0.0, eliminating them from contributing to the image."[^2]
- "For example, data acquired from a CT scanner can often be categorized as air, soft tissue, or bone based on the density value contained in the data..."[^2]

# Transfer Function
"Typically, defining the transfer functions is the hardest part of achieving an effective volume visualization since you are essentially performing a classification operation that requires you to understand the meaning of the underlying data values."[^2]

# Footnotes
- [^1]: VTK User Guide, 7.5 Using vtkPiecewiseFunction, pg. 143.
- [^2]: VTK User Guide, 7.7 Controlling Color / Opacity with a vtkVolumeProperty, pg. 145.
- [^3]: VTK User Guide, 7.10 Cropping a Volume, pg. 150-151.