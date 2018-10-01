# UMG MultiPacker Button and Image

- MultiPacker has a Button and Image Class derived from the UMG classes. The Implementation allows set the Design from a MultiPacker Database on few steps.

- The changes are only visibles on the details panel.

[**Home Docs**](https://cheke.github.io/MultiPacker)

# MultiPacker Image

![umg-i](/MultiPacker/Images/umg-i.jpg)

- The changes are only on the Appearance Category.

- **Type Layer**: Dropdown where you can define the combination of Textures. Every Texture comes from a MultiPacker database.
```
- 1_Layer: You can set the base layer. Ex: A circle.
- 2_Layers: You can set the base and addition layer. Ex: A circle with a icon.
- 3_Layers: You can set the base, addition and detail layers. Ex: A circle with a icon and an indicator of selection.
```
![umg-i](/MultiPacker/Images/umg-ie.jpg)

## Layers

![umg-layers](/MultiPacker/Images/sc_LayersUMG.jpg)

### Base, Addition and Detail

![umg-layersexp](/MultiPacker/Images/sc_layersExpanded.jpg)

- This three subcategories have the same variables. On one time explain it. 

![umg-layers](/MultiPacker/Images/sc_layerbaseexpanded.jpg)

### Color Database

- Here you select the interior look of the Layer, can be a color or a *Tile*.

- **Database**: You select a MultiPaker Database from here to load the color *Tile*.

- **Name**: Dropdown that changes with the selected Database. Select the *Tile* from here.

### Alpha Database

- Here you select the Opacity mask of the Layer from a *Tile*.

- **Database**: You select a MultiPaker Database from here to load the Alpha/Opacity *Tile*.

- **Name**: Dropdown that changes with the selected Database. Select the *Tile* from here.

![umg-layersdatasel](/MultiPacker/Images/sc_layersMPDselection.jpg)

![umg-layersdataselname](/MultiPacker/Images/sc_layersNameSelection.jpg)

- **SDF**: This is auto set by the database.

- **Use Color**: On false gives on Raw the Texture of Color Database, on True the Color Interior Selected Fills the Shape.

- **Outline**: Activate and set a color as the Outline of the SDF Shape.

- **Edge Softness**: Gives a Soft Border on SDF Shapes, avoids aliasing.

- **Base Color Outline**: You set here an RGB color for the outline Layer. *(The Variable can be moddified via animation)*

- **Base Color Interior**: You set here an RGB color for the interior Layer. *(The Variable can be moddified via animation)*

- **Base Outline Thresold**: You set here the width of the Outline, the Outline applies inside the shape. *(The Variable can be moddified via animation)*

- **Base SDFThresold**: You set here the Thresold of the SDF, allowing thicking or growing the shape. *(The Variable can be moddified via animation)*

# MultiPacker Button

- Multipacker Button has the same variables as MultiPacker Image, only extended to the states of the button Normal, Hovered, Pressed and Disables. To a better knowledge of the ussage of the variables look at [MultiPacker Image](https://cheke.github.io/MultiPacker/Doc/Umg.md#multipacker-image)

![umg-b](/MultiPacker/Images/umg-b.jpg)

![umg-bexp](/MultiPacker/Images/umg-bexp.jpg)

- **Set Disabled Style**: Enables the use of the State Disable on the Button.

[**Home Docs**](https://cheke.github.io/MultiPacker)
