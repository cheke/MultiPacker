# Nodes Options

# Output Node

- The Output Node its the final connection of all the *Tiles*, to get the final processed Texture(s). Dont have parameters to modify and only have options on their pin connection usual as another Unreal Engine Graphs.

![OutputNode](/Images/OutputNode.jpg)

# Texture Node

- The Texture Node its the node to modify the input data *Tile* from Textures, you can select the output channel via pin o via variable selection.

![TextureNode](/Images/TextureNode.jpg)

- Details Panel

![TN-tn](/Images/TN-tn.jpg)

## Texture Node

![TN-tnexpanded](/Images/TN-tnexpanded.jpg)

- **Texture Input**: Reference to the Texture Input to work as a *Tile*.

- **SDF**: Enables process the Texture as a Signed Distant Field, usually this is for Alpha Masks.

### Tiled Options

![TN-tn-to](/Images/TN-tn-to.jpg)

- On this Subcategory you defines the Number of Columns and Rows if the Input Texture have a Tiled set of Textures inside and you want to extract then as individual *Tiles*, everyone will have a name.

- **Tiles Vertical**: Number of Columns to divide the Input Texture.

- **Tiles Horizontal**: Number of Rows to divide the Input Texture.

### Non Square Size

![TN-tn-nss](/Images/TN-tn-nss.jpg)

- This Subcategory allows set the size for Textures with different width than height, resize or modify by needs. Is enabled only if the Graph has Enabled the option *Rectangle Tiles*.

- **Rectangle Size**: Shows if *Rectangle Tiles* on the Graph are Enabled.(Only visible non editable)

- **Auto Size Fill**: Dropdown to set the size from the Inut Texture with the Option: GetTextureSize.

![TN-tn-nssex](/Images/TN-tn-nssex.jpg)

- **Set Size by Parameter**: Dropdown to set from a list of sizes a value to the vertical and the horizontal sizes.

- **Size Vertical**: Height size of the *Tile*.

- **Size Horizontal**: Width size of the *Tile*.

- **Channel Input**: Dropdown to set the channel from the Input Texture who had the information you likes. This changes automatically the pin on the Graph.

## Texture Node Tile Database

![TN-tntd](/Images/TN-tntd.jpg)

- Category where you set the name of every individual *Tile* coming from the Texture.

- **Auto Name Fill**: Dropdown who allows to get the name of the Texture to auto set as the name. 

![TN-tntd-anf](/Images/TN-tntd-anf.jpg)

- GetNameFromTexture: Get and set the name of the texture as the name of the *Tile*.

- GetNameFromTextureWithAlphaSufix: Get and set the name of the texture with an sufix alpha as the name of the *Tile*. 

- **ATex Tile Data**: Array where the information about the *Tiles* and their respectives names can be modified.

![TN-tntd-atd](/Images/TN-tntd-atd.jpg)

# Material Node

![MaterialNode](/Images/MaterialNode.jpg)

[**Home Docs**](https://cheke.github.io/MultiPacker)
