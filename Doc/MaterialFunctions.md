# Material Functions

[**Home Docs**](https://cheke.github.io/MultiPacker)

- MultiPacker has some Material Functions internal on the plugin, this Material Functions works to get the *Tile* from the Texture Output, decode the SDF with possibility of Outline.

- Some Material Functions are a combined system of minor Material Functions to get and process the Texture.

- **Mayor Material Functions**
```
- MF_Image_Color_Opacity(_M): Color and Opacity are different Tiles.
- MF_Icon_Color_opacity(_M): Color and Opacity are the same Tile.
The _M version works with the Channel method Multiple, this method requires some more process, descarted on the normal Function.
```
- **Minor Material Functions**
```
- MF_UMG_Tiled(_M): Retrieves the Tile from the Texture, Channel and or Layer(_M).
- MF_UMG_SDF: Decode an SDF, with options to have Interior Color, Outline Color, Shape size and Outline size.
The _M version works with the Channel method Multiple, this method requires some more process, descarted on the normal Function.
```
![MatFunctions](/Images/MatFunctions.jpg)


[**Home Docs**](https://cheke.github.io/MultiPacker)
