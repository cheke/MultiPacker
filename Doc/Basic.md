# Basic Knowledge

-To explain everything more easy starting from now I will use the word **Tile** as the Information of every individual Texture or Material on MultiPacker.

-The Textures are composed of four Channels RGBA corresponding to Red, Green, Blue and Alpha; the Alpha channel can be Disabled to save Texture Memory.

## Texture Outputs

### **Channels**

MultiPacker has different Options to save the Output Texture: Atlas, One, Multiple and One_Sdf(this last do the same as One but all the *Tiles* will be converted to a mask Sdf).

### Atlas

- On Atlas: every individual *Tile* make use of the channels *RGB(A)*, to save the Color information.

![atlas](/Images/atlas.jpg)

### One

- On One: the *Tiles* are saved inside a Monochromatic Channel *R, G, B, or (A)* 

![channelRGB](/Images/channelRGB.jpg)

### Multiple

- On Multiple (Experimental feature): the *Tile* is saved as a mask all gradient will be lost on the process, the *Tile* is saved inside a Channel but on a process where inside every channel will be 3 *Tiles*. I call this inception of channels *Layers*, I will explain all this method on a future to open it to the world. This method have some visual artifacts on the final *Tile* extracted, I think this method combined with an artistic feel allow to save a lot of memory and the visual artifacts will be oclused by the art.

![channelMultiple](/Images/channelMultiple.jpg)

### **Tiled and Bin Packing**

- The default Option on MultiPacker is to save the *Tiles* as Tiled, this allows you to save every *Tile* with the same size on a fast way if a resize is needed is done on the fly; Bin Packing method aka *"Rectangle Tiles"* on MultiPacker Graph is a method to save the *Tiles* with different sizes on the same Texture, this method can be used on every **Channel Method**.

![Tiled](/Images/Tiled.jpg) ![BinPack](/Images/binpack.jpg)

-SDF

-Flipbook

[**Home Docs**](https://cheke.github.io/MultiPacker)
