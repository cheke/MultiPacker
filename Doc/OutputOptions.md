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
