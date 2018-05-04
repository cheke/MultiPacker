# Output Options

The MultiPacker Graph has a lot of options to process the Output Assets and all the functions involved on the process to get the Output.

I will explain all of these by the Category and Subcategory

![categories](/Images/categories.jpg)

## Texture Size Output

On this Category you can select the Size for every individual Tile for the Default option, or if you enable *Rectangle Tiles* on the subcategory *Tiled Options* you can set the method of your choice to set the *Tiles* and set the Output Size X and Y.

 ![c_texturesizeoutput](/Images/c_texturesizeoutput.jpg)

- **Texture Tile Size Output**: Size for every *Tile* who will be saved on the Output Texture, The Size for the Output Texture is calculated by the numbers of *Tiles* and the user cant select it.

### Tiled Options

- **Rectangle Tiles**: This enables the Bin packing method, every *Tile* can have a different size and will be setted on the Output Texture by the method of BinPacking Selected.

- **Rectangle Method**: From a Dropdown of different methods you can set wath method is more convenient to you.
```
- BestShortSideFit: Positions the rectangle against the short side of a free rectangle into which it fits the best.
- BestLongSideFit: Positions the rectangle against the long side of a free rectangle into which it fits the best.
- BestAreaFit: Positions the rectangle into the smallest free rect into which it fits.
- BottomLeftRule: Does the Tetris placement.
- ContactPointRule: Choosest the placement where the rectangle touches other rects as much as possible.
```
![c_to_rectanglemethod](/Images/c_to_rectanglemethod.jpg)

```
On a future workaround and addition I will do a change on all the methods to starting to BinPacking the *Tiles* starting from the *Tiles* more bigger to smaller to allow a better allocation.
```

- **Output Size X**: From a Dropdown selection you can set the Horizontal/Width Size of the Texture Output.

- **Output Size Y**: From a Dropdown selection you can set the Vertical/Height Size of the Texture Output.

![c_to_outputsize](/Images/c_to_outputsize.jpg)

## Output Config

![c_oc](/Images/c_oc.jpg)

### Channels Options

![c_oc_channelOptions](/Images/c_oc_channelOptions.jpg)

- **Channel Method**: From a Dropdown selection you can select the method to save the *Tiles* on the Output Texture.
The Methods are explained here [Basic Knowledge](https://cheke.github.io/MultiPacker/Doc/Basic).

![c_oc_channelOptions-expanded](/Images/c_oc_channelOptions-expanded.jpg)

- **Alpha**: This Enables or Disables the Alpha Channel on the Output Texture.

### Save Data

This Subcategory manages the creation of the MultiPacker Database and Material Collection Assets from the Graph, you can deselect then and dont be created and saved. By default are enabled.

![c_oc_savedata](/Images/c_oc_savedata.jpg)

- **Save Material Collection**: Enables the creation of the Material Collection Asset with the Data from the Graph.

- **Save Database**: Enables the creation of the Database Asset with the Data from the Graph.

### Location

Location has some variables to change the destination location where the Output Assets will be saved and the base name for all of them.

![c_oc_location](/Images/c_oc_location.jpg)

- **Target Directory**: This variable will open a window where you will select the desired location to save the Assets.

- **Target Name**: Variable to set the Base Name for all the Assets created by the Graph the Assets will differ with their prefix.

### Prefix

This allows you to change the Prefix on the created Assets to mantain a constant *Naming Convention* on your project.

![c_oc_prefix](/Images/c_oc_prefix.jpg)

- **Edit Prefix**: Enables change the Prefix.

- **Database Prefix**: Change the Prefix for the MultiPacker Database Aseet.

- **Texture Prefix**: Change the Prefix for the Output Texture Asset.

- **MaterialCollection Prefix**: Change the Prefix for the Material Collection Asset.

### RenderTargets Internal

Here you set the Pixel Quality for the Render Targets invilved on the Creation of the Output Texture; the Internals of this process will be described on a future.

![c_oc_renderTargetInternal](/Images/c_oc_renderTargetInternal.jpg)

- **Edit RT**: Enables change the RenderTargets.

- **RT Pixel Format**: Changes the format for the Rendertargets, this is intended to people who needed it, I dont have information about the ussage of the variables, can be enabled on special scenarios.

 ![c_oc_renderTargetInternal-expanded](/Images/c_oc_renderTargetInternal-expanded.jpg)

### Texture Output

Here you can change the parameters for the Output Texture(s)

![c_oc_textureOutput](/Images/c_oc_textureOutput.jpg)

- **Edit Texture**: Enables change parameters for the Texture(s).

- **Texture Filter**: Filter to apply on the Output Texture. The *Multiple* Channel Method requires *Nearest*.

- **Tex SRGB**: Enables the ussage of SRGB color. *SDF*, *Multiple* requires this disabled. 

The Unreal Engine Explanation is:
```
Sets whether the Texture should be gamma (un)corrected or not. Regular diffuse Textures and basically anything you use for display as color values should have this set to true. It is usually disabled for cases where the Texture color values have a specific meaning and you rely on those values to be that way as they were set, e.g. via code. Normal maps should have this set to false as their color values are to be interpreted as a direction and thus should not be gamma corrected.
```

- **Tex Address X**: Sets the addressing mode of the Texture's X axis.

- **Tex Address Y**: Sets the addressing mode of the Texture's Y axis.

- **Tex Power**: Dropdown for how to pad the texture to a power of 2 size (if necessary).

[**Home Docs**](https://cheke.github.io/MultiPacker)
