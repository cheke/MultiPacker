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

```
- GetNameFromTexture: Get and set the name of the texture as the name of the *Tile*.
- GetNameFromTextureWithAlphaSufix: Get and set the name of the texture with an sufix alpha as the name of the *Tile*. 
```

- **ATex Tile Data**: Array where the information about the *Tiles* and their respectives names can be modified.

![TN-tntd-atd](/Images/TN-tntd-atd.jpg)

- **Tile Texture**: Preview RenderTarget of the *Tile*, shows up after the graph is processed.

- **Tile Name**: Name editable of the *Tile*.

# Material Node

- The Material Node its the node to modify the input data *Tile* from the Material or Material Instance, the Material Node has some variables in common with the Texture Node.

![MaterialNode](/Images/MaterialNode.jpg)

- Details Panel

![TM](/Images/TM.jpg)

## Material Node

![TM-mn](/Images/TM-mn.jpg)

- **Material Base Input**: Reference to the Material or Material Instance Input to work as a *Tile*.

- **SDF**: Enables process the Material as a Signed Distant Field.

- **Material Instance**: Can be enabled to made a Instance from the Material Base and Change the Parameters on the Details Panel.

### Tiled Options

- On this Subcategory you defines the Number of Columns and Rows if the Input Material have a Tiled set of Textures inside and you want to extract then as individual *Tiles*, everyone will have a name.

- **Atlas**: Enable this is you like to get from the Material more than one *Tile*.

- **Tiles Vertical**: Number of Columns to divide the Input Material.

- **Tiles Horizontal**: Number of Rows to divide the Input Material.

### Non Square Size

- This Subcategory allows set the size for Material with different width than height, resize or modify by needs. Is enabled only if the Graph has Enabled the option *Rectangle Tiles*.

- **Rectangle Size**: Shows if *Rectangle Tiles* on the Graph are Enabled.(Only visible non editable)

- **Set Size by Parameter**: Dropdown to set from a list of sizes a value to the vertical and the horizontal sizes.

- **Size Vertical**: Height size of the *Tile*.

- **Size Horizontal**: Width size of the *Tile*.

## Material Node Parameters

![TM-mnp](/Images/TM-mnp.jpg)

- Category where the Material expand their Parameters to be modified, the modification can be done by a timer also, explained better on **Material Node Time Parameters**.

- **Material Button**: Dropdown who apply the changes on the material.
```
- Material updated: Default position.
- Dirty: shows where a change was done but not applied.
- Apply changes: Apply the changes done and set the Dropdown to the Default position.
```
- **Num Prints**: Number of Prints of the Material to be done (intended to work with time activated (also better explained on **Material Node Time Parameters**)).

### Parameters Array

- Subcategory where all the parameters of the Material shows and can be modified.

- **Vector Parameter**: Array with the Vector Parameters of the Material.

```
- Parameter Name: Name of the Vector (Non editable).
- Default Vector Value:
- Value Changes on Time:
- Max Vector Value:
```

- **Texture Parameter**: Array with the Texture Parameters of the Material.

```
- Parameter Name: Name of the Texture (Non editable).
- Texture: Texture Input editable to change.
```

- **Scalar Parameter**: Array with the Vector Parameters of the Material.

```
- Parameter Name: Name of the Scalar (Non editable).
- Default Value:
- Value Changes on Time:
- Max Value:
```
## Material Node Time Parameters

![TM-mntp](/Images/TM-mntp.jpg)

- Category to Change the Time Parameter on the Material. Not the *Material Time node*, this is a scalar node named Time on the Material to work with this method to simulates the *Material Time node* and allows print the Material between times or on a specified time.

- **Time Parameter**: Enable to can change the Period or the Specific Time.

- **Period**: Time is a linear increment from 0 to Period(default 1), here you defines the Period.

- **Specific Time**: Enable to use the Period as a Static Time Parameter.

## Material Node Tile Database

![TM-mntdb](/Images/TM-mntdb.jpg)

- Category where you set the name of every individual *Tile* coming from the Material.

- **Auto Name Fill**: Dropdown who allows to get the name of the Material to auto set as the name. 

```
- GetNameFromTexture: Get and set the name of the Material as the name of the *Tile*.
- GetNameFromTextureWithAlphaSufix: Get and set the name of the Material with an sufix alpha as the name of the *Tile*. 
```

- **AMat Tile Data**: Array where the information about the *Tiles* and their respectives names can be modified.

- **Tile Texture**: Preview RenderTarget of the *Tile*, shows up after the graph is processed.

- **Tile Name**: Name editable of the *Tile*.

[**Home Docs**](https://cheke.github.io/MultiPacker)
