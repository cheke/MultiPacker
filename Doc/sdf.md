# Signed Distant Field on MultiPacker

- The real power of MultiPacker are beyond the Material baking and the Texture Packing, MultiPacker has a lot of functions based on the ussage of SDF and MSDF.

## MultiPacker allows two forms of generate SDF:

**-1** Resides on the Texture Node and on the Material Node, this method are coded on c++ internally and has been coded to Multicore Performance, at the moment dont have options to change the internal parameters.
  
  ![sc_sdftexture](/MultiPacker/Images/sc_sdftexture.jpg)
  
  ![sc_sdfMaterial](/MultiPacker/Images/sc_sdfMaterial.jpg)
  
**-2** Are accesible via Material Instance, this was the initial method an works totally on gpu, some integrated GPUs crashes with some of the higher values, for that I take this method as a personal choice, The Base Material are located on the Plugin Content,  "Material / Base" Folder.

![sc_sdfMaterial](/MultiPacker/Images/sc_materialsdf.jpg)

- You can create a Material Instance from this Material and drop on the Multipacker Graph to have a SDF Mask with the Variables changed at your choice.
  
- The Material are based on this Article from Ryan Brucks : https://shaderbits.com/blog/various-distance-field-generation-techniques
  
![sc_sdfMaterial](/MultiPacker/Images/sc_SDFMaterialShow.jpg)

**Parameters Explanation**:

-**Texture Size**: Always use a Par Number, only to avoid artifacts, a range from 16 to 512 can work easily bigger values can crash.
   
-**Radius**: Its the Size of the near pixels to calculate the distance field. Values acceptables can be from 4 to "Texture Size/ 4", the bigger values have an higher increment of performance.
   
-**Tex**: Texture Input to calculate the Signed Distance Field.

-**Channel Input**: Threat as a boolean activation on channels, you can choice from RGBA channels, more than two channels selected can do artifacts and some unexpected results.

# Multi Signed Distance Field on MultiPacker

- MSDF its a more advanced technique of SDF, based on the thesis and work of Viktor Chlumsky https://github.com/Chlumsky/msdfgen .
The Technique works with vector graphics as SVG, I made a repository on Github with the code from MsdfGen compiled to x86-64, and a bat file to select and process a SVG on a few clicks, The quality of the results are better than SDF on a great number of scenarios.

   https://github.com/cheke/Msdf_BatSelector
   
 # What Use:

- After read the next part you need to know I used only SDF and MSDF from the Sizes of 16 to 64 pixels, to save the maximun possible of memory ussage.
 
-To solve some questions I can tell my personal ussage on my projects:

## -**SDF**:

-**Pros**:
- Its easy to Iterate.
- If you want to combine some masks SDF from the same Texture its fast and easy. I want it to maintain the exact position of the image.
- Works with every Texture.
- Can be done internally on MultiPacker.

-**Cons**:
- The Definition of the shape can be loosed on some cases. The resolution can be increassed but its out of my scope do it.

-**Best Scenario**:To nomal shapes on a Videogame you can use SDF.

## -**MSDF**:

-**Pros**:
- The deffinition and shape can be exactly to the SVG.

-**Cons**:
- Shapes need to be clear with few bezier curves, more complicated need more resolution.
- If you like extract some layers from the SVG its difficult, manually needs to be done and the layers will be dealigned from the original SVG.
- Only works with SVG.
- The iterations are harder.
- Need to be processed via the compiled MSDFgen and imported to Unreal Engine.

-**Best Scenarios**:To a number of special Icons you can use MSDF and Logotypes.

[**Home Docs**](https://cheke.github.io/MultiPacker)
