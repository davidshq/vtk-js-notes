# vtkAbstractVolumeMapper
- "A `vtkAbstractVolumeMapper` subclass is responsible for the volume rendering process and ensures that the input data is of the correct type for the mapper’s specific algorithm."[^1]
- Superclass for both `vtkVolumeMapper` and `vtkUnstructuredGridVolumeMapper`
- `SetInput`

# vtkColorTransferFunction
- "For the scalar value to color mapping, a `vtkColorTransferFunction` can also be used to define RGB rather than grayscale colors."[^2]
- `AddRGBPoint`
- `AddHSVPoint`

# vtkImageData

# vtkPiecewiseFunction
- "From a user’s point of view, `vtkPiecewiseFunction` has two types of methods—those that add information to the mapping, and those that clear out information from the mapping."[^2]
- "When information is added to a mapping, it is considered to be a point sample of the mapping with interpolation used to determine values between the specified ones."[^2]

# vtkVolume
- "A `vtkVolume` is used in place of a `vtkActor` to represent the data in the scene. Just like the vtkActor, the vtkVolume represents the position, orientation and scaling of the data within the scene."[^1]
- "However, a `vtkVolume` contains references to a `vtkVolumeProperty` and a `vtkAbstractVolumeMapper`."[^1]
- "A `vtkVolume` is a subclass of `vtkProp3D` intended for use in volume rendering."[^2]
- `GetColorChannels` - Returns the number of color channels (1 for grayscale, 3 for color).
- `GetGrayTransferFunction` - Returns the `vtkPiecewiseFunction` object used for grayscale.
- `GetGradientOpacity`
- `GetRGBTransferFunction` - Returns the `vtkColorTransferFunction` object used for color.
- `SetScalarOpacity` - Accepts a `vtkPiecewiseFunction` object.
- `GetScalarOpacity` - Returns the `vtkPiecewiseFunction` object used for opacity.
- `SetMapper` - Accepts subclass objects of `vtkAbstractVolumeMapper`.
- `SetProperty` - Accepts subclass objects of `vtkVolumeProperty`.
- `SetColor` - Accepts either a `vtkPicewiseFunction` (grayscale) or a `vtkColorTransferFunction` (color).
- `SetGradientOpacity`

# vtkVolumeMapper
- `CroppingOn`
- `SetCroppingRegionPlanes`
- `SetCroppingRegionFlagsToSubVolume`
- `SetCroppingRegionFlagsToFence`
- `SetCroppingRegionsFlagsToInvertedFence`
- `SetCroppingRegionFlagsToCross`
- `SetCoppingRegionFlagsToInvertedCross`

# vtkVolumeProperty
- "The `vtkVolumeProperty` represents those parameters that affect the appearance of the data in a volume rendering process, which is a different set of parameters than those used during geometric rendering."[^1]

# Footnotes
- [^1]: VTK User Guide, Chapter 7 Volume Rendering, pp. 139-140.
- [^2]: VTK User Guide, Chapter 7 Volume Rendering, pp. 143-144.