# Signed Distant Field on MultiPacker

- The real power of MultiPacker are beyond the Material baking and the Texture Packing, MultiPacker has a lot of functions based on the ussage of SDF and MSDF.

- MultiPacker allows two forms of generate SDF:

  1. Resides on the Texture Node and on the Material Node, this method are coded on c++ internally and has been coded to Multicore Performance, at the moment dont have options to change the internal parameters.
  
  ![sc_sdftexture](/MultiPacker/Images/sc_sdftexture.jpg)
  
  ![sc_sdfMaterial](/MultiPacker/Images/sc_sdfMaterial.jpg)
  
  2. Are accesible via Material Instance, this was the initial method an works totally on gpu, some integrated GPUs crashes with some of the higher values, for that I take this method as a personal choice, The Base Material are located on the Plugin Content,  "Material / Base" Folder.

  ![sc_sdfMaterial](/MultiPacker/Images/sc_materialsdf.jpg)

  - You can create a Material Instance from this Material and drop on the Multipacker Graph to have a SDF Mask with the Variables changed at your choice.
  
  - The Material are based on this Article from Ryan Brucks : https://shaderbits.com/blog/various-distance-field-generation-techniques
  
  ![sc_sdfMaterial](/MultiPacker/Images/sc_SDFMaterialShow.jpg)

  **Parameters Explanation**:

   -**Texture Size**: Always use a Par Number, only to avoid artifacts, a range from 16 to 512 can work easily bigger values can crash.
   
   -**Radius**: Its the Size of the near pixels to calculate the distance field. Values acceptables can be from 4 to "Texture Size/ 4", the bigger values have an higher increment of performance.
   
   -**Tex**: Texture Input to calculate the Signed Distance Field.

  -**Channel Input**: Threat as a boolean activation on channels, you can choice from RGBA channels, more than two channels selected can do artifacts and some unexpected results.
   
  [**Home Docs**](https://cheke.github.io/MultiPacker)
