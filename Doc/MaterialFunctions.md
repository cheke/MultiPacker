# Material Functions

[**Home Docs**](https://cheke.github.io/MultiPacker)

- MultiPacker has some Material Functions internal on the plugin, this Material Functions works to get the *Tile* from the Texture Output, decode the SDF with possibility of Outline.

- Some Material Functions are a combined system of minor Material Functions to get and process the Texture.

## Mayor Material Functions
```
- MF_Image_Color_Opacity(_M): Color and Opacity are different Tiles.
- MF_Icon_Color_opacity(_M): Color and Opacity are the same Tile.
The _M version works with the Channel method Multiple, this method requires some more process, descarted on the normal Function.
```
## Minor Material Functions
```
- MF_UMG_Tiled(_M): Retrieves the Tile from the Texture, Channel and or Layer(_M).
- MF_UMG_SDF: Decode an SDF, with options to have Interior Color, Outline Color, Shape size and Outline size.
The _M version works with the Channel method Multiple, this method requires some more process, descarted on the normal Function.
```
![MatFunctions](/MultiPacker/Images/MatFunctions.jpg)

## Description on details

### MF_Image_Color_Opacity(*_M*)

![mfimagecoloropacity](/MultiPacker/Images/mfimagecoloropacity.jpg)

- **Color_Channel(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Channel to get the *Tile*. Ex: Red = 1,0,0,0 , Alpha = 0,0,0,1 .

- **Color_Layers(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Layer to get the *Tile* (only for the method Multiple). Ex: A = 1,0,0,0 , C = 0,0,1,0 .

- **Color_BooleansTiled(V3)**: (Vector3) *(Required by _M Version)*

Bypass on a vector booleans to get the final *Tile*. vector.channel>0 = true , Red(Default)= Atlas , Green = *Tile* set on a Channel, Blue = *Tile* set on a Layer (only for the method Multiple).

- **Color_Texture(T2d)**: (Texture sample) *(Required by both)*

Texture Sample who have the Output *Tiles* of MultiPacker.

- **Color_SizePadding(V4)**: (Vector4) *(Required by both)*

Vector precalculated where indicates the location on the Texture of the *Tile*.

- **ColorInterior(V3)**: (Vector3)

Color to fill the interior of the shape.

- **ColorOutline(V3)**: (Vector3)

Color to fill the Outline of the shape (only works on SDF *Tiles*).

- **Color_IsSdf(S)**: (Scalar) *(Required by both)*

Indicates if the Color Shape is a SDF. Boolean bypass on a Scalar, 0 = false (Atlas), 1 = true (SDF), 2 = Color.

- **Opacity_IsSdf(S)**: (Scalar) *(Required by both)*

Indicates if the Opacity Shape is a SDF. Boolean bypass on a Scalar, 0 = false, 1 = true.

- **EdgeSoftness(S)**: (Scalar)

Level of softness on the border of the SDF Shape.

- **OutlineThresold(S)**: (Scalar)

Width of the Outline for the SDF Shape.

- **SdfOutline(S)**: (Scalar)

Boolean bypass on a Scalar, 0 = false, 1 = true. 

- **SDFThresold(S)**: (Scalar)

Width of the Shape of the SDF.

- **Emissive (Output)**: (Vector3)

Color Output.

- **Opacity (Output)**: (Scalar)

Alpha/Opacity Output.

### MF_Icon_Color_opacity(*_M*)

![mfcoloropacity](/MultiPacker/Images/mfcoloropacity.jpg)

- **Color_Channel(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Channel to get the Color *Tile*. Ex: Red = 1,0,0,0 , Alpha = 0,0,0,1 .

- **Color_Layers(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Layer to get the Color *Tile* (only for the method Multiple). Ex: A = 1,0,0,0 , C = 0,0,1,0 .

- **Color_BooleansTiled(V3)**: (Vector3) *(Required by _M Version)*

Bypass on a vector booleans to get the final Color *Tile*. vector.channel>0 = true , Red(Default)= Atlas , Green = *Tile* set on a Channel, Blue = *Tile* set on a Layer (only for the method Multiple).

- **Color_Texture(T2d)**: (Texture sample) *(Required by both)*

Texture Sample who have the Output *Tiles* of MultiPacker.

- **Color_SizePadding(V4)**: (Vector4) *(Required by both)*

Vector precalculated where indicates the location on the Texture of the Color *Tile*.

- **ColorInterior(V3)**: (Vector3)

Color to fill the interior of the shape.

- **ColorOutline(V3)**: (Vector3)

Color to fill the Outline of the shape (only works on SDF *Tiles*).

- **Color_IsSdf(S)**: (Scalar) *(Required by both)*

Indicates if the Color Shape is a SDF. Boolean bypass on a Scalar, 0 = false (Atlas), 1 = true (SDF), 2 = Color.

- **Opacity_IsSdf(S)**: (Scalar) *(Required by both)*

Indicates if the Opacity Shape is a SDF. Boolean bypass on a Scalar, 0 = false, 1 = true.

- **EdgeSoftness(S)**: (Scalar)

Level of softness on the border of the SDF Shape.

- **OutlineThresold(S)**: (Scalar)

Width of the Outline for the SDF Shape.

- **SdfOutline(S)**: (Scalar)

Boolean bypass on a Scalar, 0 = false, 1 = true. 

- **Opacity_Channel(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Channel to get the Opacity *Tile*. Ex: Red = 1,0,0,0 , Alpha = 0,0,0,1 .

- **Opacity_Layers(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Layer to get the Opacity *Tile* (only for the method Multiple). Ex: A = 1,0,0,0 , C = 0,0,1,0 .

- **Opacity_BooleansTiled(V3)**: (Vector3) *(Required by _M Version)*

Bypass on a vector booleans to get the Opacity *Tile*. vector.channel>0 = true , Red(Default)= Atlas , Green = *Tile* set on a Channel, Blue = *Tile* set on a Layer (only for the method Multiple).

- **Opacity_Texture(T2d)**: (Texture sample) *(Required by both)*

Texture Sample who have the Output *Tiles* of MultiPacker.

- **Opacity_SizePadding(V4)**: (Vector4) *(Required by both)*

Vector precalculated where indicates the location on the Texture of the Opacity *Tile*.

- **SDFThresold(S)**: (Scalar)

Width of the Shape of the SDF.

- **Emissive (Output)**: (Vector3)

Color Output.

- **Opacity (Output)**: (Scalar)

Alpha/Opacity Output.

### MF_UMG_Tiled(*_M*)

![mftilesdf](/MultiPacker/Images/mftilesdf.jpg)

- **Channel(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Channel to get the *Tile*. Ex: Red = 1,0,0,0 , Alpha = 0,0,0,1 .

- **Layers(V4)**: (Vector4) *(Required by _M Version)*

Defines on a vector the Layer to get the *Tile* (only for the method Multiple). Ex: A = 1,0,0,0 , C = 0,0,1,0 .

- **Booleans_encoded(V3)**: (Vector3) *(Required by _M Version)*

Bypass on a vector booleans to get the final *Tile*. vector.channel>0 = true , Red(Default)= Atlas , Green = *Tile* set on a Channel, Blue = *Tile* set on a Layer (only for the method Multiple).

- **Texture(T2d)**: (Texture sample) *(Required by both)*

Texture Sample who have the Output *Tiles* of MultiPacker.

- **SizePadding(V4)**: (Vector4) *(Required by both)*

Vector precalculated where indicates the location on the Texture of the *Tile*.

- **Emissive (Output)**: (Vector3)

Color Output.

### MF_UMG_Tiled(*_M*)

![mfSDF](/MultiPacker/Images/mfSDF.jpg)

- **ChannelTexture(V3)**: (Vector3)

*Tile* processed.

- **EdgeSoftness(S)**: (Scalar)

Level of softness on the border of the SDF Shape.

- **OutlineThresold(S)**: (Scalar)

Width of the Outline for the SDF Shape.

- **Color(V3)**: (Vector3)

Color to fill the interior of the shape.

- **Outline(V3)**: (Vector3)

Color to fill the Outline of the shape.

- **Sdf_Outline(S)**: (Scalar)

Boolean bypass on a Scalar, 0 = false, 1 = true. 

- **SDFThresold(S)**: (Scalar)

Width of the Shape of the SDF.

- **Emissive (Output)**: (Vector3)

Color Output.

- **Opacity (Output)**: (Scalar)

Alpha/Opacity Output.

[**Home Docs**](https://cheke.github.io/MultiPacker)
