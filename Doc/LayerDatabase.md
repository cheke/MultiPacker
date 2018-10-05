# Layer Database

[**Home Docs**](https://cheke.github.io/MultiPacker)

## Creating a New Layer Database

- Navigating to your Content Browser, click Add New and go to the MultiPacker category.

![Marketplace](/MultiPacker/Images/sc_newasset.jpg)

- Select Layer Database.

![Marketplace](/MultiPacker/Images/sc_newlayerdatabase.jpg)
![Marketplace](/MultiPacker/Images/sc_newlayerdatabaseselected.jpg)

## Editor Layout

![Marketplace](/MultiPacker/Images/sc_layerdatabaselayout.jpg)

1. Toolbar Menu

    An explanation of the different buttons:
    
    1.1. "Save" this saves the Graph

    1.2. "Browse" Show on the Content Browser where is the MultiPacker Graph Asset.
    
2. Details Panel

  On this Panel you have a set of variables to change the Style of the asset, all the changes are reflected on realtime on the preview panel.

3. Preview Panel

  This show an Material to Preview the Style reflecting the changes made on the Details Panel

## Details Panel

## Appearance

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

- **Color Outline**: You set here an RGB color for the outline Layer. *(The Variable can be moddified via animation)*

- **Color Interior**: You set here an RGB color for the interior Layer. *(The Variable can be moddified via animation)*

- **Outline Thresold**: You set here the width of the Outline, the Outline applies inside the shape. *(The Variable can be moddified via animation)*

- **SDFThresold**: You set here the Thresold of the SDF, allowing thicking or growing the shape. *(The Variable can be moddified via animation)*

## Use on UMG

- Use the LayerDatabase Asset on a UMG Componeent from MultiPacker is fast and easy

- Example of use with MultiPacker Image component.

![umg-layersdatasel](/MultiPacker/Images/sc_layerdatabaseImage.jpg)

- You can select from a list the LayerDatabase asset or drop it.

![umg-layersdatasel](/MultiPacker/Images/sc_layerdatabaseImageselection.jpg)

- With the asset Selected automatically the parameters are filled and changed.

![umg-layersdatasel](/MultiPacker/Images/sc_layerdatabaseimageselected.jpg)

- The Only parameters who need interaction are the Booleans "Use Color" and "Outline" to activate it.

![umg-layersdatasel](/MultiPacker/Images/sc_layerdatabaseimagesetbools.jpg)

[**Home Docs**](https://cheke.github.io/MultiPacker)
